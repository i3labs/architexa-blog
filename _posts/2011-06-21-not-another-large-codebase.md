---
id: 265
title: Uh oh, not another Large Code Base!
date: 2011-06-21T15:38:57+00:00
author: novita
excerpt: I came across two blog posts which agree that large code bases are a hassle to programmers. The first post, “Code’s worst enemy” written by Steve Yegge, basically loathes large code bases and Jeff Atwok shares the same opinion in “Size is the enemy” . The problem with large code bases is that their physical size is indication for the large amount of effort, cost and time to be invested for that project, as stated in Steve McConnell books.
layout: post
guid: http://blog.architexa.com/?p=265
permalink: /2011/06/not-another-large-codebase/
wpbb_sync_comments:
  - 'yes'
categories:
  - Developer Tools
  - Java
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<img class="alignright size-medium wp-image-276" title="question mark" src="{{site.baseurl}}/assets/uploads/2011/06/question-mark-300x197.jpg" alt="" width="300" height="197" srcset="{{site.baseurl}}/assets/uploads/2011/06/question-mark-300x197.jpg 300w, {{site.baseurl}}/assets/uploads/2011/06/question-mark.jpg 500w" sizes="(max-width: 300px) 100vw, 300px" />

I came across two blog posts which agree that large code bases are a hassle to programmers. The first post, [“Code’s worst enemy”](http://steve-yegge.blogspot.com/2007/12/codes-worst-enemy.html) written by Steve Yegge, basically loathes large code bases and Jeff Atwok shares the same opinion in [“Size is the enemy”](http://www.codinghorror.com/blog/2007/12/size-is-the-enemy.html). The problem with large code bases is that their physical size is indication for the large amount of effort, cost and time to be invested for that project, as stated in Steve McConnell books.

<!--more-->

What I find questionable is the suggestion by Yegge and Atwok that the solution for dealing with gigantic, monstrous code bases is by compressing the code base by moving on to use dynamic languages instead of Java. To quote Jeff, the problem with Java being a statically typed language, is that it requires a lot of “tedious, repetitive boilerplate code” to get things done.

Yes, coding using dynamic language does indeed shorten the code base because it does away with all the variable declarations and what not. But, [remember that we still need to write more code for unit tests to replace compilers.](http://stackoverflow.com/questions/42934/whats-with-the-love-of-dynamic-languages/43072#43072) Moreover, [less code does not imply less complexity](http://www.manageability.org/blog/stuff/less-code-less-complexity). **Dynamic languages have their own problems**; their implicitness and levels of abstraction. Such features make it unsuitable for a project where there are many developers in the team, making it almost impossible to switch to using dynamic languages.

[<img class="alignright size-full wp-image-269" title="uh oh large code base" src="{{site.baseurl}}/assets/uploads/2011/06/uh-oh-large-code-base.jpg" alt="" width="350" height="469" srcset="{{site.baseurl}}/assets/uploads/2011/06/uh-oh-large-code-base.jpg 350w, {{site.baseurl}}/assets/uploads/2011/06/uh-oh-large-code-base-223x300.jpg 223w" sizes="(max-width: 350px) 100vw, 350px" />]({{site.baseurl}}/assets/uploads/2011/06/uh-oh-large-code-base.jpg)

**Like it or not, large code bases are here to stay.** [In his attempt to shorten his code in 18 revisions](http://maurits.wordpress.com/2011/06/16/less-code-matters/), Maurits Rijk only managed to shrink it by 40%. Yes, 40% is not that bad, we still have a smaller code in the end. But he is dealing with a relatively small code with only 62 LOC orignially. Imagine if our original code base has lets say, 1 million LOC, a reduction of 40% leaves us with 600kLOC which is still quite large.

In fact, the problem with large code bases is actually the amount of time wasted. According to Peter Hallam, more than 70% of a developer’s time is spent understanding code.

**I believe that a thorough understanding of the code base itself is a more direct solution to deal with large code bases.** A comprehension of the code base helps prevent duplication and makes it easier to maintain the code. We are afraid of maintaining large code bases because we do not fully understand the code to the core. After all, we fear what we do not understand.

Now, this question naturally follows: **how can we begin to understand a ginormous code base?**

The most traditional way is by printing the source code, read and comment on the code by the paper-and-pen method. Another way is by firing up the application and then interrupt it in the debugger to catch it or stepping through the code in debug mode. The problem with these approaches is that they waste a lot of precious time that could have been better spent coding.

The greatest programmers like to automate tasks either by means of tools that are available or by writing their own script. So, why stick to traditional approaches if we can have a good, fully running script that can complete the task more efficiently?

**The good news is that there are tools available that can help us to process and digest such large code bases.** An example of such tools is Architexa, which is able to create high level UML diagrams from the source code. What I like about it is that it processes the code base and churns out neat UML diagrams. What I mean by neat is that it doesn’t throw us a huge web of dependencies like a class diagram which would have been almost useless because the visualization is almost as complicated as the code base.

We humans are visual creatures; it is much easier for us to understand the code by viewing virtual representation of the code. Personally, I prefer using such tools because they are efficient at helping me understand large code bases a lot faster. They make large code bases much less of a hassle.

<div style="clear:both;">
  &nbsp;
</div>