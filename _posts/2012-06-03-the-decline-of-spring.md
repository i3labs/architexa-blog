---
id: 384
title: The Decline Of Spring?
date: 2012-06-03T17:00:43+00:00
author: Abhishek Rakshit
layout: post
guid: http://blog.architexa.com/?p=384
permalink: /2012/06/the-decline-of-spring/
wpbb_sync_comments:
  - 'yes'
categories:
  - Java
  - 'Libraries &amp; Frameworks'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img src="assets/uploads/2012/10/springsource_logo.gif" alt="" title="springsource_logo" width="235" height="83" class="alignright size-full wp-image-388" />](assets/uploads/2012/10/springsource_logo.gif)I was recently talking to someone I respect very highly about the Spring Framework. I told him that that I would only very reluctantly consider it for a project.

Now, I have used Spring in the past, and am really a big fan of what they have done. But, these days, I keep thinking of &#8216;bloated&#8217; in association with them, and wonder if their best days are perhaps behind them.<!--more-->

**Bloatware?**

My instinct is that the root of the problem is that SpringSource built a lot of great frameworks, and as they got adopted by developers put them under the simple banner of &#8216;Spring&#8217;. Perhaps Spring being an all-encompassing name for everything done by SpringSource is the problem. Yes, this must be a major &#8216;marketing win&#8217;, but as a developer it is hard to figure out where one part of Spring starts and where it ends.

For the most recent web based service that I was building, we considered using [Netty](https://netty.io/), [Jersey](http://jersey.java.net), [Atmosphere](https://github.com/Atmosphere/), and [Play Framework](http://www.playframework.org/). Yes, those are really comparing apples and oranges, but examining these frameworks gave us a really good idea as to what was the best fit for our situation. When we decided we wanted to use something similar to Jersey, we spent a little time comparing it with others like [RESTEasy](http://www.jboss.org/resteasy). The thing is, we did not consider any of the Spring Frameworks.

The thing is that we realized that today we have so many open source frameworks that it would be very easy to get a lot of such 3rd-party code into our projects. And adding such frameworks would result in us needing to support and therefore understand the code. So instead of us using multiple large frameworks that do a lot but have various limitations we felt that it made the most sense to use the &#8216;best of breed&#8217; for whatever we were including.

**Framework Dependencies and Modularity**

Now, we did get to a point where we wanted to add a couple of &#8216;social&#8217; features, and we found that Spring Social looked to be one of the more interesting options. But adding it to our codebase meant that not only did we need to be careful in seeing how many of the other Spring Frameworks it dragged in, but that we also needed to seriously consider strategies to make sure that our entire code was insulated from the framework &#8211; so that an average developer did not need to know all the details of Spring.

I do want to add that I believe that the challenge here is really not modularity. The Spring Framework has done a great job here. The problem is that when using one particular framework from Spring, you end up needing to &#8216;adjust&#8217; your usage because of the other frameworks.

Again, I do want to say that most of us on our team are comfortable with Spring. However, it is irresponsible of us as Software Engineers to add code that is not needed. We need our code to be maintainable at the end of the day.

But the fact that Spring has evolved into a set of inter-connected frameworks hurts me in using it. I would love to see Spring evolve into sharply defined frameworks.

**Evolution&#8230;**

The interesting thing is that the challenges in using Spring today are really part of what made Spring really good a few years ago. It really is a question of how fast Spring will evolve to the changing nature of Open Source Java Framework Ecosystem.

What gives me hope is that Spring&#8217;s growth was partly because of the bloatware in JavaEE. It was in large part the success of Spring that drove JavaEE to become more lightweight. Perhaps it will be the success of these open source frameworks that will drive Spring to focus on the strengths of the independent frameworks as opposed to the single mega-framework.

**Update:** Comments have been closed to prevent knee-jerk responses that do not address the issue. If you have a good response, please e-mail me (vineet at architexa dot com). If it does address the main point here, I will make sure it gets to be a top level blog post.

<div style="clear:both;">
  &nbsp;
</div>