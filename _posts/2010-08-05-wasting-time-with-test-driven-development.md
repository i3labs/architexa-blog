---
id: 121
title: Wasting Time With Test Driven Development?
date: 2010-08-05T19:51:29+00:00
author: Vineet Sinha
layout: post
guid: http://blog.architexa.com/?p=121
permalink: /2010/08/wasting-time-with-test-driven-development/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Agile &amp; Development Methodologies'
  - 'Design Patterns &amp; Architecture'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<span style="font-size: 13.1944px;"><a href="/assets/uploads/2010/08/test.jpg"><img class="alignright size-medium wp-image-122" title="test" src="/assets/uploads/2010/08/test-300x225.jpg" alt="" width="300" height="225" srcset="/assets/uploads/2010/08/test-300x225.jpg 300w, /assets/uploads/2010/08/test.jpg 500w" sizes="(max-width: 300px) 100vw, 300px" /></a>Many teams are moving to test driven development and very often this a good thing. In a drive towards increased code stability and maintainability, good test cases can be very helpful. But this is not always the case; while working with development teams, most teams seem to have one or more critical problems. It seems that it is easy to do Test Driven Development (TDD) badly &#8211; below are five situations that I have seen multiple times.</span>
  
<!--more-->


  
<span style="font-size: 13.1944px;"><strong>1. The Drive for Code Coverage</strong></span>

<span style="font-size: 13.1944px;">One of the teams that I worked with had been effectively outsourcing development. As a metric towards doing effective development they focused on making sure that they had high code coverage. While this was a good goal, a number of their developers wrote test cases which just called the new code to execute it and then did not do anything with the results. The test cases would all end with &#8216;Assert(true)&#8217; and therefore would always have passing test cases.</span>

<span style="font-size: 13.1944px;"><strong>2. The Absence of User Feedback</strong></span>

A software system with plenty of unit tests is generally considered to be well tested. But it is often all too easy to ignore what is being tested. <span style="font-size: 13.3333px;">In TDD the unit tests only point to specific potential problem areas in the projects. Getting user feedback ensures that the features being added (and the specs as defined by the tests) are actually easy to use.</span>

**<span style="font-weight: normal; font-size: 13.1944px;"><strong>3. Excuse for lack of Documentation</strong></span>**

TDD is very helpful  in understanding code and figuring out what should be going on. But it can never replace quality documentation. Unit tests are just one aspect of a well documented project. Well maintained UML Diagrams, inline class and method descriptions, as well as architecture guidelines are needed to easily figure out the most important use cases, the key core, and the high level architecture.

<p style="font-size: 13.1944px;">
  <strong>4. Letting Architecture Decay</strong>
</p>

Often codebases that rely heavily on TDD are slower to refactor when the need arises. It becomes more difficult to modify the architecture when you need to update your test cases. A young project with swiftly changing use cases will need the flexibility to rapidly switch architecture whenever necessary. It should not be put off based on the number of unit tests that will need to be updated.

<span style="font-size: 13.1944px;"><strong>5. A roadblock to &#8216;innovation&#8217;</strong></span>

Sometimes doing new things means that you don&#8217;t know what the result will look like, how well your algorithms will work, or whether the caching will be fast enough. In such cases it is hard to have all the specifications (tests) written upfront. Often tests have to be written well after the experimental phase of a new component is completed. Waiting to create tests until you have a clearer picture of an innovative component will save many headaches and test rewrites.

<span style="font-size: 13.1944px;"><strong>Others?</strong></span>

The above is just a list of some of the more common forms of problems caused by applying test driven development that I have encountered. Have you found any others? Have you figured out a way to make sure teams stay on track?

photo credit: [flickr](http://www.flickr.com/photos/sercasey/324341982/)

<div>
</div>

<div style="clear:both;">
  &nbsp;
</div>