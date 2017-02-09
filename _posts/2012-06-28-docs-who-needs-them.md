---
id: 355
title: 'Docs- Who needs them?'
date: 2012-06-28T15:43:00+00:00
author: Christopher Deschenes
layout: post
guid: http://blog.architexa.com/?p=355
permalink: /2012/06/docs-who-needs-them/
wpbb_sync_comments:
  - 'yes'
categories:
  - Developer Tools
  - 'Documentation &amp; Communication'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

Software documentation is one of those things that is sorely missed when it isn&#8217;t there.  Why is it the last thing that any of us developers wants to do?  It seems that it is easy for us to ignore documenting in the heat of the situation, but we always get burned in one of many ways.

<p style="text-align: center;">
  <a href="/assets/uploads/2012/06/docmaps1.gif"><img class="aligncenter size-large wp-image-358" title="Literate Programming Style Code View" src="/assets/uploads/2012/06/docmaps1-1024x251.gif" alt="Literate Programming Style Code View" srcset="/assets/uploads/2012/06/docmaps1-1024x251.gif 1024w, /assets/uploads/2012/06/docmaps1-300x73.gif 300w, /assets/uploads/2012/06/docmaps1.gif 1093w" sizes="(max-width: 1024px) 100vw, 1024px" /></a>
</p>

<!--more-->

There are two situations that I get hammered with often.

## Colleagues

Ever need to fix code written by someone who is long gone?  We need code comments especially when trying to _understand_ code that someone else wrote.  Sometimes the code itself is not so easy to grok.  Its kind of like the textbook explanation that jumps over a bunch of important steps by saying &#8220;the rest is left to the reader.&#8221;  I guess that&#8217;s OK if the developer knows the requisite knowledge for the topic.  It is  unlikely that years from now when you are long gone that your code will be easily understood by the poor programmer who has to figure out what is wrong with it.

## API Users

Ever try to use a library without an example to refer to?  When using an API we usually don&#8217;t have the time to do a deep dive into the code that we need to use.  We just need to understand the calling conventions and order of method invocation.  There are cases where we may  want to be able to do a deep dive into the source code.  Code comments are then important.  But the majority of us who are usinf APIs need documentation that is more geared towards tutorials, workflows, tips and tricks, and examples.  These artifacts if done well accomplish a number of objectives.

<p style="padding-left: 30px;">
  <strong><em>Users are More Likely to Give it a Try-</em></strong><br /> If you have good documentation upfront we will be more likely to dive in and try your project.  If not it  looks like your project is not quite ready for prime time.  I wouldn&#8217;t want to become dependent on it and most likely neither will developers.
</p>

<p style="padding-left: 30px;">
  <strong><em>Ease for New Developers-</em></strong><br /> For new projects on the open source side, we have a developer&#8217;s attention for a limited time only.  If they have to work a lot to unlock the value we have provided they&#8217;ll just go elsewhere and mutter something like &#8212; alpha.  If there is an easy to understand example that ideally comes close to what the user is trying to do then that&#8217;s a win-win.  For proprietary projects it is more a matter of getting proficient with the code more quickly.
</p>

<p style="padding-left: 30px;">
  <strong><em>API Inconsistencies-</em></strong><br /> Code evolves.  But when the API documentation does not evolve with it and downstream developers are dependent on it all sorts of bad things can happen.  Consider a case where distributed teams are working on separate components of a system. Usually the various components talk across APIs.  Each team may not have a view of the source code of the other modules.  If they do perhaps it is out of date.  Let&#8217;s say there are hundreds of changes over a week or two.  Demo day looms.  Testing uncovers a major problem.  Which module is it?  Finger pointing begins.  Perhaps  the definition of a field was changed in an API and the consumer wasn&#8217;t made aware of it.  These kinds of bugs can be pretty tricky to root out.  The situation could have probably been averted by using smarter tools that keep documentation in sync with code.
</p>

By investing the time and effort into generating quality documentation on both sides of an API, you can avoid a lot of problems and put out a higher quality product.

Here&#8217;s a link to an interesting paper that analyzes what information we developers typically need to be efficient.   <strong id="internal-source-marker_0.04903030535206199"><a href="http://research.microsoft.com/en-us/um/redmond/groups/hip/papers/ko2007bugfixing.pdf">http://research.microsoft.com/en-us/um/redmond/groups/hip/papers/ko2007bugfixing.pdf</a></strong>

<div style="clear:both;">
  &nbsp;
</div>