---
id: 289
title: 'Code Visibility: one factor of code quality that you shouldn’t forget'
date: 2011-07-13T16:23:47+00:00
author: Xin
layout: post
guid: http://blog.architexa.com/?p=289
permalink: '/2011/07/code-visibility-one-factor-of-code-quality-that-you-shouldn%e2%80%99t-forget/'
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Agile &amp; Development Methodologies'
  - 'Design Patterns &amp; Architecture'
  - Developer Tools
  - 'UML &amp; Diagramming'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<img class="alignright" src="https://lh6.googleusercontent.com/oKJR11ClVJMdj2JnG5KelnHPZlmcqSqAi7pecWKq8l_kMpThLKeZP81Ij9pZzB_UYu7NWwPS4O7WoNdBPVcEvxJHlnLeE2b8mjz58_UnjcmSKB-scXs" alt="" width="360" height="229" />

Every developer cares about code quality. But how do you maintain code quality throughout the software development cycle? Readability, modularity, and efficiency all are important factors of writing good code but there isn&#8217;t much agreement on the best way to maintain a high level of code quality. 

One factor which is often missed in discussions is code visibility, or making sure your code has a clear structure so that others can easily understand it. (Take a look at the diagram above for some of the difficulties encountered when there is a lack of code visibility).
  
<!--more-->


  
Good code visibility is especially important for large projects and teams. It improves the project’s understandability, maintainability and usability which have a large influence on <a href="http://en.wikipedia.org/wiki/Software_quality#Software_quality_factors" target="_blank">software quality</a>.

There are lots of articles talking about improving your own code&#8217;s visibility:

  * [Improving code readability with css](http://coding.smashingmagazine.com/2008/05/02/improving-code-readability-with-css-styleguides/)
  * [Improving code quality](http://java.dzone.com/articles/improving-code-quality)
  * [Development tips to improve your code quality](http://www.webmonkey.com/2010/10/development-tips-to-improve-your-code-quality/)
  * [How to increase code quality](http://stackoverflow.com/questions/1205153/how-to-increase-code-quality)

But the real question is when you are given a code that is terribly written, what can you do to quickly improve its visibility?

One of the most effective ways is drawing diagrams. It used to take time; but there are now tools to help you draw diagrams and use them to understand the code.

With diagrams one can highlight major dependencies and components of the code, so that team members have an accurate view of the large parts of the code. Such as the below example of the architecture of the JDT codebase. 

  
<span>View more <a target='_blank' href='http://www.codemaps.org'>Architectural Documentation</a> on <a target='_blank' href='http://www.codemaps.org/s/Eclipse_JDT'>Eclipse JDT</a> </span>

Diagrams can add visibility to the original code. They offer a blueprint of the software product and make it easy to detect and correct errors shown in the diagrams and then rewrite the code to improve quality.

Diagrams can also help make good documentation, which helps a lot when you need to do a code review, when new team members come onboard, or when returning to code you haven&#8217;t seen in months. Hence the code quality won’t deteriorate as development continues, and as software architecture is updated by different developers.

Moreover, it’s often easier to misunderstand code than well created diagrams drawn in a standard notation. Some tools also allow diagrams, the code and Javadoc to be shared securely online. All these can help teams in collaborating, so that code quality can be improved for large projects and open source projects taken by developers with different backgrounds and geographic locations.

Well diagrammed code will help improve code visibility. And this, in turn, improves code quality.

The only problem with creating diagrams is in maintaining them and making sure that they don&#8217;t get out of date. What if there were a class of tools that were connected with the code? What if they could let you know as soon as a diagram got out of date? 

We have been working hard at work in building such a tool and would love to hear your thoughts.

<div style="clear:both;">
  &nbsp;
</div>