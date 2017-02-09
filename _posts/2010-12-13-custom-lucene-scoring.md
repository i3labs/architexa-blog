---
id: 175
title: Custom Lucene Scoring
date: 2010-12-13T17:14:44+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=175
permalink: /2010/12/custom-lucene-scoring/
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

[<img class="alignright size-full wp-image-166" title="lucene_green_300" src="assets/uploads/2010/11/lucene_green_300.gif" alt="" width="300" height="46" />](http://lucene.apache.org/)When you have a lot of data, finding what you are looking for can be a challenge. Fortunately, Google and other search engines help us make sense of the vast amount of data on the web. But what about your own data? Lucene is a great tool for indexing and searching large amounts of information quickly. Fundamentally it uses a great deal of intelligence to determine which Documents are most important to you based on your query. On the surface Lucene is easy to set up and provides many useful benefits, and taking a peek under the hood can give us insight into the core of Lucene&#8217;s powerful features.

I have covered the basics of [indexing](http://blog.architexa.com/2010/11/getting-started-with-lucene-creating-an-index/) and [searching](http://blog.architexa.com/2010/12/getting-started-with-lucene-searching-your-index/) in Lucene. For those of you interested in the internal workings of Lucene there is no better place to start than its scoring system. Lucene&#8217;s brain is its Scoring system. This critical calculation is what determines which results are returned from your searches. Depending on the type of data you are indexing and the purpose of your application you may want to implement a custom method of scoring your data. For instance, when searching data about used cars you may want to put more weight on make and model than, say, color.

<!--more-->

**Scoring Variables**

Lucene&#8217;s default scoring system works very well for most cases. It uses seven different variables to determine the final ranking of each document. They are: (from [lucenetutorial.com](http://www.lucenetutorial.com/advanced-topics/scoring.html))

>   * tf = term frequency in document = measure of how often a term appears in the document
>   * idf = inverse document frequency = measure of how often the term appears across the index
>   * coord = number of terms in the query that were found in the document
>   * lengthNorm = measure of the importance of a term according to the total number of terms in the field
>   * queryNorm = normalization factor so that queries can be compared
>   * boost (index) = boost of the field at index-time
>   * boost (query) = boost of the field at query-time

These factors are fed into the Similarity algorithm, details of which can be found in Lucene&#8217;s [java-doc](http://lucene.apache.org/java/3_0_0/api/core/org/apache/lucene/search/Similarity.html) and [tutorial](http://lucene.apache.org/java/3_0_0/scoring.html) pages. For the moment I will focus on the simplest method for adjusting scoring: &#8220;Boost&#8221;.

**Boost**
  
Boost increases the weight of a specific field or document so that it will be more likely to be returned by relevant queries. This is a simple way to adjust Lucene&#8217;s default behavior; the only tricky part is determining when and where to add boost.

If you are boosting the value of an entire document you&#8217;re going to have to set its boost before the document is indexed. `document.setBoost(3.5)` This will make all the fields in this document 3.5 times more likely to appear in search results.

If you are only interested in increasing the chances of a single field being found by a query then you have two options: you can set the fields boost before it is added to the document, or you can add boost when performing a query. To set the boost during indexing do the following: `field.setBoost(1.4)` This works in much the same way as document boosting shown above. Remember that field boost will be compounded with any boost given to the document it is added to. Boosts added during indexing are more efficient but if you are searching for data and you want to give a specific Query clause more importance you might want to consider Query boosting. For example if you have a query for &#8220;big red chevy truck&#8221; you might want to boost &#8220;chevy&#8221; because make may be the most important.
  
`<br />
Query query = parser.parse("chevy");<br />
query.setBoost(2.0);<br />
Query[] query2 = parser.parse("big red truck");`

**Extending the Similarity Class**

More ambitious users may want to implement their own version of Lucene&#8217;s Similarity class. This will allow for fine grained control of the algorithm calculating the scores of you documents. You can easily remove any of the variables listed above or add custom calculations to suit your needs. For example:

`<br />
class IsolationSimilarity<br />
&nbsp;&nbsp;extends DefaultSimilarity {<br />
&nbsp;&nbsp;&nbsp;&nbsp;public IsolationSimilarity(){}<br />
&nbsp;&nbsp;&nbsp;&nbsp;public float idf(int docFreq, int numDocs) {<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return(float)1.0;<br />
&nbsp;&nbsp;&nbsp;&nbsp;}<br />
&nbsp;&nbsp;&nbsp;&nbsp;public float coord(int overlap, int maxOverlap) {<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return 1.0f;<br />
&nbsp;&nbsp;&nbsp;&nbsp;}<br />
&nbsp;&nbsp;&nbsp;&nbsp;public float lengthNorm(String fieldName, int numTerms) {<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return 1.0f;<br />
&nbsp;&nbsp;&nbsp;&nbsp;}<br />
}<br />
` 
  
[source](http://www.wortcook.com/pdf/lucene-ranking.pdf)

This code shows how by overriding specific Similarity methods you can ignore the calculations done by those sections. In this case by returning &#8216;1&#8217; we are ignoring document frequency (idf), term coordination(coord), and term field normalization(lengthNorm). Therefore in this search we don&#8217;t care how much a term appears across the index, how many of the terms in the query were found in in the document, or how many terms are in the field. By ignoring these factors we are ranking documents solely on how often the searched for term appears in the document and any boost on the document/field.

  
<span>View more <a target='_blank' href='http://www.codemaps.org'>Architectural Documentation</a> on <a target='_blank' href='http://www.codemaps.org/s/Lucene'>Lucene</a></span>

**Thoughts**

Experimenting with the scoring system in Lucene may seem intimidating at first, but with a little patience you can customize it to provide much more benefit to your application. Just like each data set and index is unique, each tool used to search them should also be equally unique.

Please let us know if there are any other Lucene topics you would like us to cover.

<div style="clear:both;">
  &nbsp;
</div>