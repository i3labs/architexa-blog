---
id: 54
title: The Waterfall Model is not all bad (and some lessons for agile teams)
date: 2010-05-03T06:37:35+00:00
author: Vineet Sinha
layout: post
guid: http://blog.architexa.com/?p=54
permalink: /2010/05/waterfall-model-not-all-bad-and-lessons-for-agile-teams/
categories:
  - 'Agile &amp; Development Methodologies'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-medium wp-image-57" title="real_waterfall" src="{{site.baseurl}}/assets/uploads/2010/04/real_waterfall-231x300.jpg" alt="" width="231" height="300" srcset="{{site.baseurl}}/assets/uploads/2010/04/real_waterfall-231x300.jpg 231w, {{site.baseurl}}/assets/uploads/2010/04/real_waterfall.jpg 385w" sizes="(max-width: 231px) 100vw, 231px" />]({{site.baseurl}}/assets/uploads/2010/04/real_waterfall.jpg)The Waterfall model has become a [joke](http://www.waterfall2006.com/) and is pointed to as an way of doing software development poorly. While the approach has a number of limitations, it is helpful in some situations. Understanding these situations can be useful when trying to use an agile development methodolgy to make sure that you do not make critical mistakes.

During a conversation last week, a team lead told me that he considered Agile and Watefall as being two different approaches with the same result. As a proponent of Agile approaches, I tried to understand his situation and convince him of the benefit of an agile approach. After some discussion, I came to the conclusion that his situation was unique in that it actually benefit from a more rigid approach.

<!--more-->

The reality is that different development methodologies are appropriate for different situations. And while we all have our favorite approaches, we need to be careful about whether our current team/project benefits or gets hurt by our choice of development methodologies. Agile approaches breakdown [without strong collaboration](http://blog.architexa.com/2010/04/developer-responsibility-in-agile-teams/), and a waterfall approach cannot deal with changing requirements.

While the Waterfall model (even when first [described](http://en.wikipedia.org/wiki/Waterfall_model#cite_ref-0)) was used as an example of a flawed development model, it does have strengths. Many organizations need better software systems, but don&#8217;t really understand their requirement. Having a well-defined process for gathering requirements can help clarify the most important parts of a complex project. Agile teams work well when faced with changing requirements but they need to make sure **that the first requirements that they are working on are the most important ones**.

<div id="attachment_55" style="width: 310px" class="wp-caption alignright">
  <a href="{{site.baseurl}}/assets/uploads/2010/04/waterfall1.png"><img class="size-medium wp-image-55" title="waterfall1" src="{{site.baseurl}}/assets/uploads/2010/04/waterfall1-300x297.png" alt="" width="300" height="297" srcset="{{site.baseurl}}/assets/uploads/2010/04/waterfall1-300x297.png 300w, {{site.baseurl}}/assets/uploads/2010/04/waterfall1-150x150.png 150w, {{site.baseurl}}/assets/uploads/2010/04/waterfall1.png 363w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    Agile development may not be as efficient when progressing towards a known goal (as indicated by the red line), but they do have useful functionality in every iteration.
  </p>
</div>

<div id="attachment_56" style="width: 304px" class="wp-caption alignright">
  <a href="{{site.baseurl}}/assets/uploads/2010/04/waterfall2.png"><img class="size-medium wp-image-56 " title="waterfall2" src="{{site.baseurl}}/assets/uploads/2010/04/waterfall2-294x300.png" alt="" width="294" height="300" srcset="{{site.baseurl}}/assets/uploads/2010/04/waterfall2-294x300.png 294w, {{site.baseurl}}/assets/uploads/2010/04/waterfall2.png 363w" sizes="(max-width: 294px) 100vw, 294px" /></a>
  
  <p class="wp-caption-text">
    Goals change over time - a team using the waterfall model will take much longer to reach an adjusted goal than an agile one.
  </p>
</div>

The benefit of knowing all the requirements of a complex project can be a big strength of the Waterfall model. While having all the requirements does mean that the team needs to know both the problem and the solution, having this information allows optimizing how modules interact and therefore reduces the [high communication overhead](http://en.wikipedia.org/wiki/The_Mythical_Man-Month) in projects. While Agile teams thrive in situations where only the problem is known, they do this at a cost &#8211; that of not having as clear module definitions, having code duplications, and thus having a higher communication overhead among development team members. Agile teams therefore **need to make sure that they are consistently [paying down techincal debt](http://www.codinghorror.com/blog/2009/02/paying-down-your-technical-debt.html) and improving the code based on an updated-architecture**.

Additionally, knowing all the requirements in a project allows for teams following a waterfall model to optimize development efficiency by not worrying about short-term feature milestones that are not needed in the complete system. While this can add significant integration challenges for non agile teams when deploying an entire working system, the presence of the short-milestones in agile teams can add significant overhead for agile teams. Agile teams therefore need to realize that their lack of such development efficiency do comes with a benefit &#8211; one of having shorter milestones to **provide their customers useful functionality frequently and therefore needing to focus on having working code with real users in each milestone**.

<small>Image credit: <a href="http://www.flickr.com/photos/hamed/462658709/" target="_blank">flickr</a></small>

<div style="clear:both;">
  &nbsp;
</div>