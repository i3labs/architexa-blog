---
id: 104
title: Implications of limited understanding in code..
date: 2010-07-15T23:50:54+00:00
author: Vineet Sinha
layout: post
guid: http://blog.architexa.com/?p=104
permalink: /2010/07/implications-of-limited-understanding-in-code/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Documentation &amp; Communication'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<div style="float: right; margin: -5px 0 -5px 10px;">
  <a href="http://www.architexa.com/images/AgileandErosion.png"><img class="alignright" style="border: 0px initial initial;" src="http://www.architexa.com/images/AgileandErosion.png" border="0" alt="" width="300" height="200" /></a></p> 
  
  <p>
    <a title="Challenges of Software Development Cycle" rel="prettyPhoto" href="http://www.architexa.com/images/AgileandErosion.png"><br /> </a>
  </p>
</div>

We know that programmers do spend a [lot of time understanding code](http://blog.architexa.com/2010/05/no-you-are-not-dumb-programmers-do-spend-a-lot-of-time-understanding-code/). But what is not discussed as much are the implications of this limited understanding.

The reality of implementing new features or just fixing bugs is that the architecture of our underlying system continues to change. With time pressures to deliver such code updates, code changes often need to be made without thorough understanding and as development continues the code quality deteriorates. As such development continues, the system grows into a state where the &#8220;Cost of Change&#8221; rises rapidly over time, and the inability to meet user needs leads to the failure of many projects.<!--more-->

I encountered problems a little while back while trying to provide better zooming support for the [Architexa Suite](http://www.architexa.com). I was able to get the zooming feature working but later found out that I had introduced a bug causing a different feature to break. While our tests caught the bug, without a detailed understanding of the code easily available I was unable to understand the underlying architectural layers sufficiently. This caused me to re-implement zooming and ended up taking me more time and just causing endless frustration in making sure the architecture for both features were correct.

Insufficient understanding of code often causes a number of problems depending on what you are doing:

<ul style="margin-left:20px">
  <li>
    While designing, local decisions are often made resulting in brittle architectures.
  </li>
  <li>
    While coding, being unable to identify clear module/abstraction boundaries results in new code being placed in incorrect locations/modules causing an erosion of the code architecture.
  </li>
  <li>
    While testing, the absence of architectural information results in a difficulty in being thorough with the various components and often results in undiscovered bugs making way into releases.
  </li>
</ul>

**Understanding is a Team challenge**
  
Having a clear understanding of code is imperative in maintaining its quality. But we often need to work with code that we encounter which is hard to understand and lacks visibility. One large cause is usually that **code visibility is hard for more than just for us (individual developers), it is a challenge faced by the entire team**. A common solution for teams is often by performing code reviews. When a developer makes changes, a code review can help refine the implementation. In such cases it is often helps for multiple team members to share and discuss a clear picture of the current implementation, the changes that need to be made, and how such changes are consistent with the project as a whole.

Beyond such &#8216;collaborative&#8217; needs, teams often have limited documentation of a project&#8217;s core parts. When working on our own codebase it is often easy to think of the code being written as easy to understand. However, as multiple developers perform code changes such lack of documentations makes understanding code even harder &#8211; and makes it almost impossible to even product good documentation. A team&#8217;s development gets slowed down due to poorly documented and spaghetti-like code. Which force the team back to spending larger amounts of time on understanding in the future. The opposite end of the spectrum is also a challenge &#8211; when teams try to ensure thorough documentation, it is easy for such documentation to get out-of-date and teams need to spend more time just keeping diagrams up to date.

**Thoughts & Summary**
  
Understanding code can take alot of effort on a code-base but it is often worth it, otherwise the code quality deteriorates very fast. Documentation often helps &#8211; but you often need to balance carefully between having very limited documentation (which is not helpful) and having too much (which gets out of date). If you are feeling like you are spending alot of time understanding the code, perhaps it is worth working with your team to stop the architectural deterioration before it gets to be a big problem for everyone.

<div style="clear:both;">
  &nbsp;
</div>