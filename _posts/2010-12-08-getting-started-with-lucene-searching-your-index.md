---
id: 174
title: 'Getting Started with Lucene: Searching your Index'
date: 2010-12-08T08:25:53+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=174
permalink: /2010/12/getting-started-with-lucene-searching-your-index/
wpbb_sync_comments:
  - 'yes'
categories:
  - Java
  - 'Libraries &amp; Frameworks'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-full wp-image-166" title="lucene_green_300" src="{{site.baseurl}}/assets/uploads/2010/11/lucene_green_300.gif" alt="" width="300" height="46" />]({{site.baseurl}}/assets/uploads/2010/11/lucene_green_300.gif)As humans, we are constantly being bombarded with data throughout our lives. Thanks to the superb filtering and attention abilities of our brains we are able to make sense of all this information. Java programs and web apps need to rely on Lucene for this ability. Using Lucene, apps can now collect information at will, add it to an index, and retrieve whatever information is currently needed quickly and efficiently.

In my [last post](http://blog.architexa.com/2010/11/getting-started-with-lucene-creating-an-index/) we learned the basics of creating and modifying a Lucene Index. Now I&#8217;ll give you some tips on how to query your index and avoid some of the pitfalls and stumbling blocks I&#8217;ve come across.
  
<!--more-->


  
**Searcher**

The first step in searching an index is to open the index with a IndexSearcher and IndexReader. These work in conjunction to open the Index in read-only mode, allowing you to safely search it.

`<br />
IndexReader reader = IndexReader.open(FSDirectory.open(new File(index)), true); // only searching, so read-only=true<br />
Searcher searcher = new IndexSearcher(reader);<br />
` 

If you are not constantly updating your index it is a good idea to only open the IndexSearcher once. This will save you processing time and allow you to start a new Query at any time with the same IndexSearcher. On the other hand, if you Index is constantly being updated you may want to close and re-open your IndexSearcher in order to capture a new snapshot of your index.

**Querys and QueryParsers**

To run a search on you Index, you need a QueryParser and a Query that can be understood by the IndexSearcher. To create a QueryParser you must instantiate it using the same Analyzer that the documents in your index were created with.

`<br />
Analyzer analyzer = new StandardAnalyzer(Version.LUCENE_CURRENT);<br />
QueryParser parser = new QueryParser(Version.LUCENE_CURRENT, field, analyzer);<br />
` 

In this example the StandardAnalyzer was used to add documents to the index so it is being used again here to retrieve them. The parameter &#8216;field&#8217; can be a string representing a field name. It specifies the default field that will be used when the query doesn&#8217;t explicitly specify a field. QueryParser can also be extended to parse queries in a custom manner.

Just as you can open an IndexSearcher once and keep it open to reduce overhead, you can also instantiate a QueryParser with a default field and an Analyzer and just keep using that same one. But QueryParser isn&#8217;t thread-safe, so you would need a separate QueryParser for each thread using the index.

Once we have a parser we can create the most important part, the query! The query is created by passing a search term(s) in the form of a string to the parser.

`<br />
Query query = parser.parse(queryText);<br />
` 

In this example the search terms are represented by &#8216;queryText&#8217;. The parser will interpret any modifiers in this string and create a corresponding Query that the searcher can understand. For example, if our search string is &#8220;sandwich -ham&#8221; then the parser will return a Query that will find tokens including &#8220;sandwich&#8221; but NOT including &#8220;ham.&#8221;

**Results**

Once we have a query we can use the searcher to find corresponding results. Depending on your version of Lucene you can use two different methods for returning results. Originally the searcher would return a list of &#8216;Hits,&#8217; this evolved into a HitCollector and now as of Lucene 3.0, just a Collector. There are plenty of examples showing how to use older versions of Lucene to return and parse Hits so I will focus on Lucene 3.0

To search with Lucene 3.0 you can use an existing collector or create your own. The collector will determine how the results will be returned, sorted, and filtered. A popular existing Collector is the TopScoreDocCollector which returns the top x number of results.

`<br />
TopScoreDocCollector collector = TopScoreDocCollector.create(10, true);<br />
searcher.search(query, collector);<br />
ScoreDoc[] docs = collector.topDocs().scoreDocs;<br />
for (int i = 0; i < docs.length; i++) {<br />
&nbsp;&nbsp;Document result = isearcher.doc(docs[i].doc);<br />
&nbsp;&nbsp;System.out.println(result);<br />
}<br />
` 

In this example we are getting the top 10 results and looping through them and printing out the results. Note that each result is a Document and can therefore display either it&#8217;s field name, value, or both.

Another method is to create your own Collector and display the data in whichever way you want. This can be slightly more intimidating but can give you much more flexibility.

`<br />
Collector streamingHitCollector = new Collector() {<br />
private Scorer scorer;<br />
private int docBase;<br />
// simply print docId and score of every matching document<br />
public void collect(int doc) throws IOException {<br />
&nbsp;&nbsp;System.out.println("doc=" + doc + docBase + " score=" + scorer.score());<br />
}<br />
public boolean acceptsDocsOutOfOrder() { return true; }<br />
public void setNextReader(IndexReader reader, int docBase) throws IOException<br />
{<br />
&nbsp;&nbsp;this.docBase = docBase;<br />
}<br />
public void setScorer(Scorer scorer) throws IOException {<br />
&nbsp;&nbsp;this.scorer = scorer;<br />
}<br />
};<br />
searcher.search(query, streamingHitCollector);<br />
` 

Here you can see we have created a collector called &#8216;streamingHitCollector&#8217; which implements some key methods. Notice that the &#8216;collect&#8217; method prints out the document and score as it is &#8216;collected&#8217; by the searcher.

**Locking the Index**

Whenever you open an index for searching or adding documents, Lucene places a file lock on the index in order to prevent concurrent writing to the same file and to prevent writing to a file while it is being searched. The Lock implementation uses file.delete(), however, which doesn&#8217;t check that the lock file is cleaned up. If something happens to prevent the lock file from being deleted (for example if the app ends unexpectedly), a stale lock file can result, causing errors when one tries to access the index. In order to release a locked file in Lucene 3.0 you must do the following:

`directory.clearLock(WRITE_LOCK_NAME);`

In this example &#8216;directory&#8217; is the directory of the index that is locked and &#8216;WRITE\_LOCK\_NAME&#8217; is the id of the lock. (typically &#8216;write.lock&#8217; when adding items to an index)

Let us know if you have any other tips or have encountered any specific problems with Lucene.

<div style="clear:both;">
  &nbsp;
</div>