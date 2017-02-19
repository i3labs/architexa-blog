---
id: 147
title: 'Focusing on Developer Needs: Architectural Design, Understanding, and Documentation'
date: 2010-11-03T15:16:07+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=147
permalink: /2010/11/focusing-on-developer-needs-architectural-design-understanding-and-documentation/
wpbb_sync_comments:
  - 'yes'
categories:
  - About
  - 'Agile &amp; Development Methodologies'
  - Developer Tools
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-medium wp-image-149" title="two" src="{{site.baseurl}}/assets/uploads/2010/11/two1-218x300.jpg" alt="" width="153" height="210" srcset="{{site.baseurl}}/assets/uploads/2010/11/two1-218x300.jpg 218w, {{site.baseurl}}/assets/uploads/2010/11/two1.jpg 384w" sizes="(max-width: 153px) 100vw, 153px" />]({{site.baseurl}}/assets/uploads/2010/11/two1.jpg)One of the nice things about <a title="And we're off!" href="http://blog.architexa.com/2010/06/and-we-are-off/" target="_blank">launching</a> a tool is the opportunity it allows in talking to our users. Over the last 3+ months we have spent a great deal of time talking to development teams about Architexa, and have gotten a great deal of insight not only into what they like and don&#8217;t like about Architexa, but more importantly, what pains they have felt. The consensus is clear: while developers do need to focus on coding on a day-to-day basis, to be successful on a long term they need to worry about the parts of the system that are shared between team members. These worries where what we focused on for the most recent release (v2) or Architexa.
  
<!--more-->

### **A New Focus**

When trying to dive into what developers wanted with these shared parts, we learned that they wanted to be effective with two things: their ‘environment’ &#8211; the frameworks and libraries that all the developers on the team need to use but typically don&#8217;t modify, and the ‘common&#8217; &#8211; all the parts of the code that are modified by two or more people. Developers wanted better support with the code architecture.

For developers, dealing with the code architecture means that they not only need to design parts of new features, but also <a href="http://www.architexa.com/" target="_blank">easily understand, describe, and manage the architecture</a>. In such situations the big technologies of the day (like UML or Collaboration) often end up slowing developers by forcing to many requirements on them. When teams are large enough to have a Software Architect, then the Architect is able to help in some of the software architecture tasks, but at the end of the day it is often more than he can handle.

At Architexa we have been examining these developer needs a lot and trying to see where we can do our bit to help. When it comes to designing features &#8211; often a whiteboard works well in making sure that every team is on the same page. But when developers need to implement the features, fix bugs, or just improve performance in a manner consistent with what they have &#8211; developers often need to spend \*alot\* of time <a href="http://www.architexa.com/technology/index" target="_blank">just going through code</a>. And beyond making sense of the project, developers often need to communicate changes to other team members &#8211; both developers as well as the business guys. We have been hearing that developers need help working with the architecture of the code that they already have &#8211; in both understanding it quickly and documenting that understanding for others.

Building an easy-to-use tool suite for helping developers understand and document their code was our first goal with Architexa. Not only did we make sure to provide easy code exploration with our class diagrams and sequence diagrams, but we also made sure to provide layered architectural diagrams built straight from the code with support to easily dive into details just by double clicking. As we built those we realized that software development is inherently collaborative, and we added support to allow developers to share diagrams straight from their IDE using a very simple collaboration server.

### **Version 2.0**

As we made the above capabilities available to users, we found developers using Architexa on larger codebases than we had initially planned. Our recent release therefore focused on improving performance. We improved indexing performance by over 50% and added sophisticated build filtering and scheduling mechanisms. We also received requests from developers for supporting additional collaboration options amongst team members, and have therefore also included many features to make sharing diagrams even easier.

  * **E-Mail Based Collaboration** &#8211; You can now share diagrams with multiple users via email. Archtiexa also keep tracks of e-mail addresses in an address book so that you access common addresses easily.
  * **Team Server** &#8211; Beyond being able to share diagrams on our secure team server, you now have the option to also have the Architexa server running inside your company&#8217;s network for use by your teams.
  * **Easier Code Review** &#8211; Architexa now provides source repository integration (SVN/ CVS) to easily document new features or review code. When making changes, you can ask Architexa to make a diagram based on any your changes.

We are eager for more feedback. How can we make Architexa better suite your needs?

<div style="clear:both;">
  &nbsp;
</div>