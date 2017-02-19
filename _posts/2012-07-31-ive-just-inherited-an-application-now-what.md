---
id: 368
title: 'I&#8217;ve Just Inherited an Application &#8211; Now What?'
date: 2012-07-31T15:13:33+00:00
author: Christopher Deschenes
layout: post
guid: http://blog.architexa.com/?p=368
permalink: /2012/07/ive-just-inherited-an-application-now-what/
wpbb_sync_comments:
  - 'yes'
categories:
  - Developer Tools
  - 'Documentation &amp; Communication'
  - Java
  - 'UML &amp; Diagramming'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<div id="attachment_369" style="width: 310px" class="wp-caption alignright">
  <a href="{{site.baseurl}}/assets/uploads/2012/07/LuceneOverviewDiag.png"><img class="size-medium wp-image-369" title="Lucene Overview Diagram" alt="Lucene Overview Diagram" src="{{site.baseurl}}/assets/uploads/2012/07/LuceneOverviewDiag-300x225.png" width="300" height="225" srcset="{{site.baseurl}}/assets/uploads/2012/07/LuceneOverviewDiag-300x225.png 300w, {{site.baseurl}}/assets/uploads/2012/07/LuceneOverviewDiag.png 602w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    What if I had a diagram like this?
  </p>
</div>

I have previously written about how lack of decent software documentation can cause problems in doing what we developers love to do, deliver functioning software. Documentation, code comments and good variable naming are all key to understanding code.  This applies to both code that we write and applications that we use through their API’s.  We could just as easily be looking at C/C++/C#, Python, PHP or any language but for now let’s stay with Java (read more about advantages of Java over other languages at [theappsolutions.com](http://theappsolutions.com) .

I want to illustrate how useful diagrams are in understanding an existing complex Java code base. Understanding code quickly is particularly important when inheriting a new project or trying to figure out how to use a third party package or open source project. As we all know we are typically faced with tight deadlines, limited resources, and herculean objectives. Sound familiar?<!--more-->

Here’s one anecdotal example of where lack of documentation and diagrams caused a particularly gnarly situation. I agreed to take on the challenge of commercializing a software package that was developed in a university lab. It was a rewrite of a federated peer-to-peer simulation system originally written in C++ on CORBA but later rewritten in Java by a team of student developers and recent graduates. The code base consisted of five high level packages, 17 subpackages, 25,000 lines of open source code and about 220,000 lines of proprietary code.

Two hundred fifty thousand lines is a lot of code. Non-trivial. Getting up to speed to the point where features can be added and current functionality improved is a formidable task. Keep in mind that the application includes some very complicated algorithm implementations. Did I mention that this is a distributed  system that provides interoperability across scientific and engineering applications?  And that the core of the system manages simulation execution and moves data from application to application at the right time in the right format sometimes involving transformations?  You start to get the picture.

These kinds of projects are notorious for lacking documentation both in code and at the user level. After all, documentation doesn’t demonstrate prowess with a particular language or framework, functioning software does. In a professional setting the situation is different. Right? Unless it is a bureaucratic (<strong id="internal-source-marker_0.20067688589915633"><a href="http://bit.ly/MHXG9y">CMM</a> </strong> level greater than 1) the situation is likely the same; aggressive deadlines, limited resources, changing requirements, and management overhead (“Is it done yet?”).

In larger organizations added complications such as countless developers with their own styles and naming conventions, legacy applications that may be years and years old but are still mission critical, create substantial barriers to quickly understanding how code works. Some applications are so complicated that no one single person truly has a deep understanding of everything going on.

As we were trying to understand the code base and communicate what it was, what it did, and how it was built to potential customers, users, and buyers we quickly discovered that there was no architectural-level documentation. No diagrams. No design documents, just the code. This was a bit of surprise for me as many of the projects I had worked on in the past that were of this scale had some documentation artifacts. In hindsight, the documentation for projects I had seen was usually grossly out of sync with the actual code if it existed at all.

This is not a new problem. Check out this <strong id="internal-source-marker_0.20067688589915633"><a href="http://bit.ly/Pn4Z8G">post</a></strong> for even more details around “software archeology”. Code Spelunking also has a lot of attention. Check out this <strong id="internal-source-marker_0.20067688589915633"><a href="http://bit.ly/MmmXp1">paper</a></strong> (you may need to login to the ACM site) for a fairly detailed discussion of code spelunking.

We ended up drawing diagrams after manually going through the code and deciding for ourselves what was important hoping that we weren’t missing anything. I did use a code analyzer to get line counts for modules. The time we spent doing this was time taken away from making a better product. This is killer in a startup or in any project for that matter! Better documentation or a toolset that could generate insightful information about the codebase would have been extremely helpful.

Follow me on twitter @Chris_Deschenes

<a href=&#8221;http://theappsolutions.com&#8221;>theappsolutions.com </a>

<div style="clear:both;">
  &nbsp;
</div>