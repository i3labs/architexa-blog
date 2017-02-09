---
id: 62
title: 'No, You are not Dumb! Programmers do spend a lot of time Understanding Code&#8230;'
date: 2010-05-05T18:49:32+00:00
author: Vineet Sinha
excerpt: While working on a codebase, developers spend a lot of time understanding code. We might be unwilling to admit it for fear of sounding dumb but the huge amount of time spent on making sense of code is staggering. In fact a conference is held every year just to tackle this problem...
layout: post
guid: http://blog.architexa.com/?p=62
permalink: /2010/05/no-you-are-not-dumb-programmers-do-spend-a-lot-of-time-understanding-code/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Design Patterns &amp; Architecture'
  - 'Documentation &amp; Communication'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img src="/assets/uploads/2010/05/Fotolia_11453646_XS.jpg" alt="" title="Understanding code" width="323" height="238" class="alignright size-full wp-image-64" srcset="/assets/uploads/2010/05/Fotolia_11453646_XS.jpg 404w, /assets/uploads/2010/05/Fotolia_11453646_XS-300x220.jpg 300w" sizes="(max-width: 323px) 100vw, 323px" />](/assets/uploads/2010/05/Fotolia_11453646_XS.jpg)While working on a codebase, developers spend a lot of time understanding code. We might be unwilling to admit it for fear of sounding dumb but the huge amount of time spent on making sense of code is staggering. In fact a <a href="http://www.program-comprehension.org/" target="_blank">conference</a> is held every year just to tackle this problem. The good news is that with the emergence of online communities more and more people are discussing the challenges of working with large codebases openly.

<!--more-->

**The Back Story**
  
About 10 years ago I was working on the Office Codebase for Microsoft. Even while implementing some really small features, it would take me a lot of time just trying to figure out how different parts of the code related to one another. As it was one of my first really large projects in the role of developer, I just quietly ended up spending the time understanding the code and hiding it from the rest of the team. I was not very experienced then and felt that it was just a personal limitation.

The cause of the problems was not the team or the bad code. It was just the simple fact that having 100+ developers writing code day-in day-out on a project means that there is a lot of code to read &#8211; even if you are only focusing on one part of the codebase. After a month or so of working on the codebase, I started to wish that I had better tools that could help me. Realizing that Microsoft would spend the money to buy a license of a good tool if I found something I was happy with, I looked for something and was quite upset to not find anything helpful.

In fact, I wanted something so much that I even wrote a tool in my spare  time (more on that in another post). As I dove more into building something useful, the project grew into a Master&#8217;s thesis and eventually a PhD thesis before I felt like I had gotten to a useful point. But as I researched the topic I was really surprised to find the significant amount of studies done on the topic.

**Results from Studies**

> **Update:** We have updated the content below and included it in a table on our website. For an easier to read page of this data see [here](http://www.architexa.com/technology/index).

An IBM <a href="http://domino.research.ibm.com/tchjr/journalindex.nsf/600cc5649e2871db852568150060213c/e19d7828ab04524285256bfa00685c14!OpenDocument" target="_blank">research</a> by Corbi in 1989 found that more than half of the effort in accomplishing a task for the programmer is towards understanding the system. Later on at Bell Labs in 1992, Davison&#8217;s team <a href="http://www3.interscience.wiley.com/journal/97518983/abstract" target="_blank">found</a> that new project members spend 60%-80% of their time understanding code, with the number dropping at most down to a low of 20% as the developers gain experience in the code that they are working with. Another <a href="http://portal.acm.org/citation.cfm?id=782010.782031" target="_blank">study</a> in 1997 at the National Research Council in Canada lead by Singer et al. found developers spending over 25% of their time either searching for or looking at code.

More recently, in 2006 a <a href="http://portal.acm.org/citation.cfm?id=1134355" target="_blank">study</a> conducted at Microsoft with 157 developers found that roughly equal amounts of time is spent understanding code as other tasks such as designing, unit testing, and writing. In 2007, a <a href="http://portal.acm.org/citation.cfm?id=1240624.1240714" target="_blank">survey</a> of over 780 developers at Microsoft conducted by a team led by Cherubini found that 95% agreed that understanding existing code is a significant part of their job. Further, over 65% indicated spending time understanding existing code at least once a day (with over 25% indicating doing it multiple times a day).

Even Peter Hellam in his <a href="http://blogs.msdn.com/peterhal/archive/2006/01/04/509302.aspx" target="_blank">blog </a> mentions that more than 70% of a developers time is spend understanding code as it is a preliminary requisite when testing code, modifying existing code or even writing new code.

**Takeaway**
  
Although many tools which help developers understand code are evolving but their effectiveness in day to day work is something yet to be determined. Till then, as developers it is our responsibility to write clear and understandable code to make life easier for anyone who will work on our codebase in future.
  
Perhaps John Woods says it best:
  
<!-- http://twitter.com/Architexa/status/13320573118 -->

<div class='bbpBox' style='background:url("http://s.twimg.com/a/1273008894/images/themes/theme1/bg.png") #ACDED6;padding:20px;'>
  <p class='bbpTweet' style='background:#fff;padding:10px 12px 10px 12px;margin:0;min-height:48px;color:#000;font-size:16px !important;line-height:22px;-moz-border-radius:5px;-webkit-border-radius:5px;'>
    &#8220;Always code as if the guy who ends up maintaining your code will be a violent psychopath who knows where you live.&#8221; <a href='http://bit.ly/d5BXYA' target='_new'>http://bit.ly/d5BXYA</a><span class='timestamp' style='font-size:12px;display:block;'><a title='Mon May 03 18:59:01 ' href='http://twitter.com/Architexa/status/13320573118'>Mon May 03 18:59:01 </a> via <a href="http://sharefeed.com" rel="nofollow">ShareFeed</a></span><span class='metadata' style='display:block;width:100%;clear:both;margin-top:8px;padding-top:12px;height:40px;border-top:1px solid #fff;border-top:1px solid #e6e6e6;'><span class='author' style='line-height:19px;'><a href='http://twitter.com/Architexa'><img src='http://a1.twimg.com/profile_images/715882826/atxa-logo-icon_normal.png' style='float:left;margin:0 7px 0 0px;width:38px;height:38px;' /></a><strong><a href='http://twitter.com/Architexa'>Architexa</a></strong><br />Architexa</span></span>
  </p>
</div>

<!-- end of tweet -->

<div style="clear:both;">
  &nbsp;
</div>