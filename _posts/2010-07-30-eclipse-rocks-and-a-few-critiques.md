---
id: 108
title: Eclipse (Helios) rocks and a few critiques
date: 2010-07-30T19:08:09+00:00
author: Vineet Sinha
layout: post
guid: http://blog.architexa.com/?p=108
permalink: /2010/07/eclipse-rocks-and-a-few-critiques/
wpbb_sync_comments:
  - 'yes'
categories:
  - Developer Tools
tags:
  - eclipse
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-full wp-image-109" title="logo-eclipse-helios" src="/assets/uploads/2010/07/logo-eclipse-helios.jpg" alt="" width="271" height="173" srcset="/assets/uploads/2010/07/logo-eclipse-helios.jpg 451w, /assets/uploads/2010/07/logo-eclipse-helios-300x191.jpg 300w" sizes="(max-width: 271px) 100vw, 271px" />](/assets/uploads/2010/07/logo-eclipse-helios.jpg)Helios has been out for over a month &#8211; and we have been using it. Yes, we are a little biased, but when you are working with and leading teams of 10+ developers you need to be practical. There are a number of things that Eclipse does really well, but there are a few things that we would like to see better.

<!--more-->

One thing worth mentioning is that the Eclipse release happened on time again. While they have done this consistently since 2003, it does get harder when you have millions of users using the tool day-to-day.

**The Basics**
  
[<img class="alignright size-medium wp-image-118" title="eclipse_autocomplete_10" src="/assets/uploads/2010/07/eclipse_autocomplete_10-300x254.png" alt="" width="210" height="178" srcset="/assets/uploads/2010/07/eclipse_autocomplete_10-300x254.png 300w, /assets/uploads/2010/07/eclipse_autocomplete_10.png 320w" sizes="(max-width: 210px) 100vw, 210px" />](/assets/uploads/2010/07/eclipse_autocomplete_10.png)
  
I use vi for most of my text editing needs &#8211; it is my default editor for pretty much everything, except Java. Eclipse (and most modern IDE&#8217;s) have done alot to make the lives of developers easier and when there are new releases it is easy to forget some of these conveniences. From finding compilation errors when you save, to pointing potential bugs as you write them &#8211; noticing errors sooner helps in implementing features. Content assist further shows you the various legal coding options to just write code faster. Beyond these, shortcuts to easily find classes or launch the application being developed help in focusing on what we care about. And then there is support for easily switching to the various views and editor tabs or the various organizations fixed by the perspectives.

**The cool new stuff**

<div id="attachment_115" style="width: 201px" class="wp-caption alignright">
  <a href="/assets/uploads/2010/07/mpc.png"><img class="size-medium wp-image-115" title="mpc" src="/assets/uploads/2010/07/mpc-245x300.png" alt="" width="191" height="234" srcset="/assets/uploads/2010/07/mpc-245x300.png 245w, /assets/uploads/2010/07/mpc.png 645w" sizes="(max-width: 191px) 100vw, 191px" /></a>
  
  <p class="wp-caption-text">
    The Eclipse Marketplace Dialog
  </p>
</div>

There are quite a few things which stand out in Helios. One of my favorites is the _MarketPlace_. Searching and adding new plugins for Eclipse have always been a challenge. The Eclipse Marketplace makes this much easier &#8211; it allows you to not only search a central location of all Eclipse plugins, but also allows you to find the most recent and the most popular plugins.

<p style="text-align: left;">
  The availability of annotations has helped remove configuration files from Java apps and resulted in the rise of the use of annotations. Eclipse now supports showing annotations with the the <em>JavaDoc hovers</em> and makes it easier to understand details of a method. Beyond annotations, it also supports showing the @value fields inlined when included in JavaDoc.
</p>

<div id="attachment_116" style="width: 310px" class="wp-caption aligncenter">
  <a href="/assets/uploads/2010/07/annotations-in-javadoc.png"><img class="size-medium wp-image-116" title="annotations-in-javadoc" src="/assets/uploads/2010/07/annotations-in-javadoc-300x146.png" alt="" width="300" height="146" srcset="/assets/uploads/2010/07/annotations-in-javadoc-300x146.png 300w, /assets/uploads/2010/07/annotations-in-javadoc.png 509w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    Annotations in JavaDoc
  </p>
</div>

[<img class="alignright size-medium wp-image-110" title="remove-from-view-action" src="/assets/uploads/2010/07/remove-from-view-action-300x183.png" alt="" width="240" height="146" srcset="/assets/uploads/2010/07/remove-from-view-action-300x183.png 300w, /assets/uploads/2010/07/remove-from-view-action.png 421w" sizes="(max-width: 240px) 100vw, 240px" />](/assets/uploads/2010/07/remove-from-view-action.png)At times when looking into the _call hierarchy_ view its gets really frustrating to find the caller you need. Helios lets you go through each caller one by one, and provides you a way to remove all those unnecessary calls from the call hierarchy view so that you can focus on those which concern you. Related to this, previously the extraction of type hierarchy information would cause the Eclipse to freeze in large projects. The recent version extracts _type hierarchies_ in background leaving you to continue your work.

<div style="float: right;">
  <a href="/assets/uploads/2010/07/progress.png"><img class="alignright size-medium wp-image-114" title="progress" src="/assets/uploads/2010/07/progress-300x50.png" alt="" width="220" height="40" /></a><br /> <a href="/assets/uploads/2010/07/overlaytext.png"><img class="alignright size-medium wp-image-113" title="overlaytext" src="/assets/uploads/2010/07/overlaytext-300x75.png" alt="" width="220" height="45" /></a>
</div>

Another cool feature in this version is the _TaskItem Overlay_. It allows you to customize the item shown in the task bar to either show you a particular text, image, or even a progress-bar. Beyond such useful information when switching applications, developers can also a menu with the item which shows when you click on it.

[<img class="alignright size-medium wp-image-112" title="bp-details" src="/assets/uploads/2010/07/bp-details-294x300.png" alt="" width="235" height="240" srcset="/assets/uploads/2010/07/bp-details-294x300.png 294w, /assets/uploads/2010/07/bp-details.png 450w" sizes="(max-width: 235px) 100vw, 235px" />](/assets/uploads/2010/07/bp-details.png)Eclipse debug views are one of the more powerful views and Helios now provides much better _breakpoint detail_ by displaying all the properties in a single pane. This support has actually been available previously but was hidden behind a context menu and many developers often do not even realize their existence. This new pane makes the features more easily discoverable and helps in reducing the time in looking for needed information on the fly.

**What&#8217;s missing**
  
So yeah, Eclipse rocks &#8211; but at the same time I am often wishing for more. The core reason is that Eclipse has a lot of features that it just feels monolithic and the interface feels complicated. While evangelizing the platform I have had way too many &#8216;what does X do&#8217; and &#8216;in many cases how can I remove X&#8217;. With Eclipse&#8217;s plugin strength it will be great to see a very simple single download to start things off and a menu to easily add (or enable) the features that I want. The Eclipse marketplace is a great start &#8211; but we need to split up Eclipse and add it the various components as features into the marketplace. If needed we can even add another tab for these basic features. Without these, Eclipse will feel heavyweight, and we should not be surprised to hear more of the &#8216;from your demo it feels like Eclipse is much faster than I thought&#8217;.

<div style="clear:both;">
  &nbsp;
</div>