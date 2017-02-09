---
id: 146
title: 'Getting started with Lucene: Creating an Index'
date: 2010-11-16T17:36:37+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=146
permalink: /2010/11/getting-started-with-lucene-creating-an-index/
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

<a href="http://lucene.apache.org" target="_blank"><img class="alignright size-full wp-image-166" title="lucene_green_300" src="assets/uploads/2010/11/lucene_green_300.gif" alt="" width="300" height="46" /></a>One of my favorite parts of working at Architexa is that I get the chance to learn and experiment with new and interesting libraries, projects, and tools. One such project is Lucene. It provides a great infrastructure for indexing and searching any sort of text. This can be used for all sorts of applications and has saved us a great deal of time when keeping track of data in our projects.

<!--more-->

One of the first steps in using Lucene is creating an index. I wanted to write down some of the main parts of this that I found interesting while learning Lucene. Hopefully this will help others that are trying to find detailed information on one of the most popular search infrastructures available.

The Index is the heart of any component that utilizes Lucene. Much like the index of a book, it organizes your data so that it is quickly accessible. An index consists of Documents containing one or more Fields. Documents and Fields can represent whatever you choose but a common metaphor is that Documents represent entries in a database table and Fields are akin to the fields in the table.

**Creating the IndexWriter**

Lucene Indexs must be created in a specific Directory and with a specific Analyzer. The Directory can be in memory but is typically a FSDirectory since most indexes are too large to store in memory. The Analyzer parses data that is added to your index into tokens so that it will be searchable. more details here: [http://lucene.apache.org/java/3\_0\_0/api/core/org/apache/lucene/analysis/Analyzer.html](http://lucene.apache.org/java/3_0_0/api/core/org/apache/lucene/analysis/Analyzer.html)

 `IndexWriter writer = new IndexWriter(FSDirectory.open("/index"), new StandardAnalyzer(Version.LUCENE_CURRENT), true, IndexWriter.MaxFieldLength.LIMITED);`

As seen above the three decisions you must make are: what directory should your index be located in, what type of Analyzer works best for your data, and the third parameter which is whether or not you want to create a new Index. NOTE If the third parameter is true you will overwrite any index currently residing in the chosen directory.

**Add a Document**

The next step is to add each Document to your index. To do this call addDocument() as shown below.

`Document document = new Document();<br />
document.add(new Field("name", "Page 1", Field.Store.YES, Field.Index.NO));<br />
document.add(new Field("text", "Lorum Ipsum...", Field.Store.YES, Field.Index.TOKENIZED));<br />
writer.addDocument(doc);`

Each document can contain as many fields as necessary and documents within the same index are not required to contain equivalent fields. For instance; an index containing webpages with fields of title, keywords, and body may also contain employees with fields of name, phone number, birthday, and address. Fields can be tagged with flags to let Lucene know whether they should be indexed, stored, or tokenized. There is a good resource for understanding this here: http://tim.oreilly.com/pub/a/onjava/2003/01/15/lucene.html?page=2#field_types

**Deleting a Document**

To remove a document from an index you must first find the document by querying it. Queries will be covered more in subsequent posts.

`writer.deleteDocuments(query);<br />
` 
  
Lucene allows duplicate documents to be added to an index. This can make updating documents more complex than simply overwriting them. In previous versions of Lucene you had to manually remove the document and then add the updated one back. Since Lucene version 2.2, you can call updateDocument(term,document) where &#8216;term&#8217; is the document(s) to be deleted gathered from a query and &#8216;document&#8217; is the updated document to be added back in.

A problem that is often encountered is a document not being deleted because its id field is tokenized. deleteDocument and updateDocument only work to remove docs containing the exact Term they&#8217;ve been given, which a doc with a tokenized id won&#8217;t contain. The solution is to make sure your doc has an id that&#8217;s untokenized. See the above section on fields for more information.

**Closing the Writer**

Finally once the changes have been submitted to the IndexWritter call the following methods:
  
`writer.optimize();<br />
writer.close();`
  
This will optimize the index for searching and make sure all the changes are recorded properly.

**Tips and Tricks**

  * When adding documents leave your writer open and only close the writer / optimize when absolutely necessary. These two methods result in a lot of overhead so be done sparingly and only when instantaneousness updating is necessary.
  * When first creating an index make sure that you pass &#8216;true&#8217; as a parameter only if you wan to create a brand new index
  * Adding Documents correctly can be tricky in some cases. Make sure to read up on the different Analyzers and Field types

Let me know if you have any questions!

<div style="clear:both;">
  &nbsp;
</div>