---
id: 155
title: 'Understanding Code Visually: Three Ways that Work'
date: 2010-11-08T16:09:13+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=155
permalink: /2010/11/understanding-code-visually-ways-that-work/
wpbb_sync_comments:
  - 'yes'
categories:
  - Developer Tools
  - 'Documentation &amp; Communication'
  - 'UML &amp; Diagramming'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-medium wp-image-161" title="understandBulb" src="/assets/uploads/2010/11/understandBulb-300x225.jpg" alt="" width="210" height="158" srcset="/assets/uploads/2010/11/understandBulb-300x225.jpg 300w, /assets/uploads/2010/11/understandBulb.jpg 800w" sizes="(max-width: 210px) 100vw, 210px" />](/assets/uploads/2010/11/understandBulb.jpg)In trying to help developers <a href="http://www.architexa.com/" target="_blank">understand code</a> we have made sure to listen to what they have to say. We&#8217;ve noticed that many developers utilize UML style diagrams to try to understand code. However many problems exist with existing tools. I have tried using a number of UML tools and found that the reverse-engineering capabilities in the majority of them were not helpful for understanding tasks. They focus on designing tasks; reverse-engineering capabilities often just end up showing convoluted pictures and lots of useless information. Even developers that commonly use these tools [ask us](http://stackoverflow.com/questions/3871449/what-tools-should-i-use-to-visualize-structure-of-my-code/3878175#3878175) how to best understand code. Of course there are many solutions to this problem and the solution varies depending on the situation.

It is important to think about which specific perspectives you need to understand. Is the structure of the codebase in a state of disrepair and needs attention? Or are underlying code concepts, features, and logic the most important? There seem to be three main types of diagrams people use to help visually understand code.

<!--more-->

**The Mile High View**: A [layered architectural diagram](http://www.architexa.com/learn-more/layered-diagrams) can be really helpful to know how the main concepts in a project are related to one another. They provide a good starting point when other resources are unavailable. Examining the relationships between packages in a project can provide a good sense of where the most important code lies. They can also give insight into projects and packages that are poorly named or organized in a counterintuitive way.

<div id="attachment_160" style="width: 310px" class="wp-caption aligncenter">
  <a href="/assets/uploads/2010/11/layered.png"><img class="size-medium wp-image-160" title="layered" src="/assets/uploads/2010/11/layered-300x145.png" alt="" width="300" height="145" srcset="/assets/uploads/2010/11/layered-300x145.png 300w, /assets/uploads/2010/11/layered-1024x496.png 1024w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    A layered diagram showing how the different components of Apache Log4J are related. You can clearly see that the components varia, chainsaw,and jmx build on top of the core interfaces and logger class along with support utils
  </p>
</div>

**The Core**: It is important to try to figure out how the code works with regards to the main concepts. [Class diagrams](http://www.architexa.com/learn-more/class-diagrams) are exceptionally useful here. Pen-and-paper works often enough, but tools can not only speed up the process but also help you save and share such diagrams. Inheritance relationships as well as class structure can become immediately apparent with a well constructed class diagram. By limiting the scope of your diagram to a specific concept you can easily avoid the problem of overwhelming, &#8220;everything but the kitchen sink&#8221; style diagrams.

<div id="attachment_159" style="width: 310px" class="wp-caption aligncenter">
  <a href="/assets/uploads/2010/11/class.png"><img class="size-medium wp-image-159  " title="classDiagramInitial" src="/assets/uploads/2010/11/class.png" alt="" width="300" height="150" /></a>
  
  <p class="wp-caption-text">
    A Class diagram showing the heirarchy model of Apache HttpClient. Specifically, the Http Methods package showing all the HttpRequest Classes. Notice that the POST and PUT requests inherit from HttpEntityEnclosingRequestBase where as GET and others do not.
  </p>
</div>

**Key Use Cases**: By tracing at least one key use case for your app you can gain a great deal of insight. You likely can get the most important use cases from anyone on your team, and stepping through them will be really helpful. Most IDE&#8217;s provide helpful solutions for quickly navigating the source. This can often be helpful for simple logic but more complex scenarios may require sequence diagrams. Some [sequence diagramming](http://www.architexa.com/learn-more/sequence-diagrams) tools allow you to focus on the most important aspects of the logic you are interested in. Complex sequences of method calls, conditionals, and loops can often be reduced to an elegant diagram that will illuminate any potential bugs or unintended consequences of your code.

<div id="attachment_158" style="width: 305px" class="wp-caption aligncenter">
  <a href="/assets/uploads/2010/11/sequence.png"><img class="size-medium wp-image-158   " title="Restaurant-UML-SEQ (1)" src="/assets/uploads/2010/11/sequence.png" alt="" width="295" height="300" /></a>
  
  <p class="wp-caption-text">
    A sequence diagram describing the procedure for searching a Lucene 3.0 index. Notice that the collect method is inside an anonymous inner class (Collector) and is responsible for actually outputting the results of the search.
  </p>
</div>

When originally confronted with the problem of understanding code visually I was left unsatisfied by the array of tools currently available. Many showed too much information or were difficult to use and were therefore unhelpful for understanding code. <a href="http://nitinbhide.blogspot.com/2010/09/rereading-mythical-manmonth-flowcharts.html" target="_blank">Some</a> say that code is inherently unable to be visualized in a useful way. We at Architexa are intent on challenging this belief. We have attempted to address the problems inherent in understanding a complex codebase by creating an easy to use dynamic visualization tool. Let us know your thoughts.

<div style="clear:both;">
  &nbsp;
</div>