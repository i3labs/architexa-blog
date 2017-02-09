---
id: 218
title: 'Making Cool Ideas Happen: Studying Our Users and Software Immigrants'
date: 2011-03-03T22:13:38+00:00
author: Abhishek Rakshit
layout: post
guid: http://blog.architexa.com/?p=218
permalink: /2011/03/making-cool-ideas-happen-studying-our-users-and-software-immigrants/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Agile &amp; Development Methodologies'
  - Developer Tools
  - User Experience
tags:
  - apache
  - eclipse
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-medium wp-image-221" title="innovation" src="assets/uploads/2011/02/innovation-300x199.jpg" alt="" width="300" height="199" srcset="assets/uploads/2011/02/innovation-300x199.jpg 300w, assets/uploads/2011/02/innovation.jpg 400w" sizes="(max-width: 300px) 100vw, 300px" />](assets/uploads/2011/02/innovation.jpg)One of the nice things about being Software Developers, is that it&#8217;s really nice to spend our time working on cool ideas:  building out systems that help in situations where no solution currently exists. The problem is that often these cool ideas fail. Yes, using an Agile approach helps significantly, especially when customers/users request features. But often customers don&#8217;t realize what problems they need solved or what developers are capable of. Skilled engineers have the opportunity to really push the envelope with new and innovative ideas. The challenge then becomes making sure that these new ideas actually meet a need.

<!--more-->

The most common problem when working on something cool, is believing in the greatness of the idea. I have seen many organizations that typically get user feedback for most projects, going into a super-secret mode to protect their cool idea. When the completed feature/product is launched and things don&#8217;t go according to plan, the product team often gets so disappointed in the product that no effort is spent refining it or management labels it a failure and kills the product resources. It is becoming more and more common to see companies address this by initially deploying to a small group of users to get feedback and using agile development practices.

**Pushing the Edge on Innovation**

But iterating on feedback and being Agile is only part of the solution. Depending on how innovative you want to be, there are a number of things that you need to do:

  * Learn the needs of the users (which we talk about here)
  * Learn about what users want as a solution to this need (will be discussed in a future post)
  * Learn about what they think of your current solution (Agile helps a lot with this)

Learning about the needs of users is important. It&#8217;s easy to live in a bubble, especially when absorbed with a great idea. Talking to even 3-4 people about the idea, and asking them which parts of idea they would consider the most important can give you a really helpful feeling of what your users would want. In trying to find and talk to those users that ‘get it’, you will better understand your users and what parts are most important to them. For example, [IMVU](http://www.imvu.com/) started as an idea to be an extension to an IM client, but found that its users considered it akin to MySpace.

Getting feedback from the first few fans of the idea helps in understanding their basic needs. At this point it can help to flesh out the idea on a larger scale. Running a simple survey can get you great results about the importantance of the problem you&#8217;re solving. Won’t it be great to respond to a customer saying, &#8220;Yes we have scheduled and want to get you your favorite feature X, but we found that 70% of users would rather have innovative feature Y, and we are making sure to get it to you first.&#8221;

**Studying Software Developers: Open Source Software Immigrants**

My ‘cool’ idea started its life when I found it extremely time consuming to make sense of the Microsoft Office codebase. I always wished that the codebase had a class hierarchy chart similar to the one that used to be available for [MFC classes](http://msdn.microsoft.com/en-us/library/ws8s10w4(v=vs.80).aspx?ppud=4). As I started thinking about it, I realized that I had more situations where I needed to get a quick high-level overview of the code and that I needed something that was easier to manage than some of the complex UML tools out there.

<div id="attachment_222" style="width: 310px" class="wp-caption alignright">
  <a href="http://msdn.microsoft.com/en-us/library/ws8s10w4(v=vs.80).aspx?ppud=4"><img class="size-medium wp-image-222 " title="mfcClass" src="assets/uploads/2011/02/mfcClass-300x228.gif" alt="" width="300" height="228" srcset="assets/uploads/2011/02/mfcClass-300x228.gif 300w, assets/uploads/2011/02/mfcClass-1024x781.gif 1024w, assets/uploads/2011/02/mfcClass.gif 1418w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    The hierarchy chart representing the MFC library. One of the sources of inspiration for Architexa
  </p>
</div>

As I started my PhD, I wanted to understand the problems that other developers faced. I found a lot of innovative tools to help developers understand but quickly realized that they were not focusing on the biggest need. Instead they were focusing on beginner programmers understanding toy pieces of code using flow charts.

In order to understand how often developers need to work with ugly code, I decided to run a study. I found that there was a special name for developers in this situation; when experienced developers are new to a project or are new to a part of a codebase they are referred to as software immigrants. Software immigrants have been previously studied by [Susan Sim](http://www.ics.uci.edu/~ses/index.html) and [Ric Holt](http://plg.uwaterloo.ca/~holt/) (see The Ramp-Up Problem in Software Projects: A Case Study of How Software Immigrants Naturalize – [1](ieeexplore.ieee.org/iel4/5475/14745/00671389.pdf?arnumber=671389) and [2](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.39.6654)), who noticed patterns on the type and schedule of ramp-up tasks as well as the impact of environmental and administrative issues. I found that with regards to understanding code they noticed ‘bottom-up comprehension strategies’ to be more effective and that the lack of documentation effected developer’s rampup.

Given the results, I wanted to understand the usefulness of various solutions. To accomplish this I created a survey consisting of a few key parts: What is your experience with the project in question?, How hard is it to understand?, What about the project made it easy to understand?, What would have made it easier?, What tasks did you perform when working with the code and how difficult would you rate them?

After talking to a couple of people I quickly realized that developers working on open source projects often work on code that they might not have seen before and that it would be great to hear their thoughts. Based on this I sent an e-mail to the various mailing lists of various Apache and Eclipse open source projects and surveyed approximately 100 developers.

The survey results helped me better understand the problems developers face and guided me towards building a set of features that is innovative, intuitive, and functional. I will describe our survey results in more detail in out next post.

<div style="clear:both;">
  &nbsp;
</div>