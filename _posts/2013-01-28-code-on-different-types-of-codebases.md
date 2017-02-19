---
id: 400
title: Code on Different Types of Codebases
date: 2013-01-28T17:36:11+00:00
author: Vineet Sinha
layout: post
guid: http://blog.architexa.com/?p=400
permalink: /2013/01/code-on-different-types-of-codebases/
categories:
  - 'Design Patterns &amp; Architecture'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<div id="attachment_401" style="width: 245px" class="wp-caption alignright">
  <a href="{{site.baseurl}}/assets/uploads/2013/01/allianz-arena-300x148.jpg"><img class="alignright size-full wp-image-401" alt="allianz arena" src="{{site.baseurl}}/assets/uploads/2013/01/allianz-arena-300x148.jpg" width="235" srcset="{{site.baseurl}}/assets/uploads/2013/01/allianz-arena-300x148.jpg 300w, {{site.baseurl}}/assets/uploads/2013/01/allianz-arena.jpg 640w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    <a href="http://www.flickr.com/photos/siebeneinhalb-de/1232149352/">Allianz Arena</a> by <a href="http://www.dirkloop.com/">Dirk Loop</a>
  </p>
</div>

A lot has been written about blogging and working on open source projects to improve your coding skills. They are great ideas. In addition, I like [attending user groups](http://blog.architexa.com/2013/01/breaking-out-of-your-shell-as-a-coder/).

But there is more. Becoming a great software developer also means making sure you are able to think as the situation demands, as opposed to being biased in the manner that your current project is developed. It means making sure you are comfortable building very different types of projects.<!--more-->

In the last few years, work has meant building Eclipse plugins, a flex based app, and a web service. However, I recently began to notice a lot of browser extensions. I wanted to see if building them had any lessons for me. Instead of trying to brainstorm random ideas, I heard of a need for our _sales_ team. A few weekends later and a lot of studying Google&#8217;s [extensions documentation](http://developer.chrome.com/extensions/), I built something. It wasn&#8217;t great, but it was helpful. Over the next few weeks, my colleagues got excited about it, and I could make improving the chrome extension to be part of my work.

I learned, and took advantage of, an interesting approach to [security for Chome extensions](http://developer.chrome.com/apps/sandboxingEval.html). While I have used Sandboxes before, writing code on both sides of the sandbox was new to me.

Building low level coding skills are easy. If you have programmed in 2-3 languages, and know how to implement a couple of algorithms, then you should be able to implement most systems. However, you are likely not going to be making the best high level decisions unless you have experience building projects of very different architectures.

Now, I do have a day job. So, I can&#8217;t spend too much time on such side projects, but there is very little that can substitute feeling the difference between building something that only has JavaScript in a few places, versus building something that is primarily JavaScript. And this difference is getting to be really important these days &#8211; especially for organizations that really try to do a good job for their users.

**Tips**

There are 3 tips that have worked very well for me, when I have been working on such projects.

**1. Think Small:** It is hard to get your boss to approve working on a fun project. While working on these projects, I knew I had a limited amount of time. I also know of all the fun projects that I want to do that are just sitting on the side. So, when I select a project to do, I work very hard to somehow scope it down so that it can be finished in a weeks worth of time. Finishing a project within 40 hours of coding time is really hard, but at least this way the project gets finished before I have gotten busy and/or bored with the project.

Oh yeah, most such projects have taken 2-3x as long as I was planning. But, isn&#8217;t that the same as the industry?

**2. Build Useful:** Beyond trying to build the project in a week, I want something that it useful to at least one person. Thinking about making this person happy not only helps me get the job done and ignore other fun things, but it also makes me focus on the coding details that will actually make the user happy (as opposed to me focusing on the interesting technical challenges). And, yes, if it does include things that I can put on my resume, then that is only for the better.

**3. Go Different:** Beyond selecting a small project, I have typically tried to do one or two things very differently about each project. This includes moving from building a desktop app, to building a server side app, to building an algorithmically intensive app, to a rich interactive browser based app. And while I do the above, why not choose a different language to make the above in?

Building an app in a new language within 40 hours is not easy. But, try it. You will quickly realize that you need to sacrifice some things that you thought were obvious, and you will feel really good when you realize that you were able to accomplish the challenge.

**Thoughts**

I have learned a lot doing the above. I had built many things with Javascript, and while I am now much better at it, I still realize that I really like having a static strongly typed language for development. And not just because the compiler effectively creates some tests from me, but also because I consider myself as an engineer, and feel the responsibility in making sure whatever I build is able to be maintained by others. Here, Microsoft&#8217;s experiment with Typescript looks really interesting, and I am putting it on my list of things to experiment with.

Have you tried something similar to the above? What&#8217;s worked for you?

<div style="clear:both;">
  &nbsp;
</div>