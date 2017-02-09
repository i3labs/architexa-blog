---
id: 74
title: Designing forms without the problem of Premature Commitment
date: 2010-05-26T18:49:04+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=74
permalink: /2010/05/designing-forms-without-the-problem-of-premature-commitment/
categories:
  - User Experience
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-medium wp-image-78" title="2232897539_1abdf7d2f8" src="/assets/uploads/2010/05/2232897539_1abdf7d2f8-300x192.jpg" alt="" width="240" height="154" srcset="/assets/uploads/2010/05/2232897539_1abdf7d2f8-300x192.jpg 300w, /assets/uploads/2010/05/2232897539_1abdf7d2f8.jpg 500w" sizes="(max-width: 240px) 100vw, 240px" />](/assets/uploads/2010/05/2232897539_1abdf7d2f8.jpg)Recently I was testing a form for uploading a diagram to a server. Entering a name and description was easy enough but choosing a group to add it to caused some frustration. I had forgotten to add a new group for my diagram! The only solution available to me was to cancel the dialog and open a different one to create the group; a frustrating procedure. Imagine how much time is wasted every day by minor frustrations like this.

Forcing a user to make decisions (uploading a diagram) before all the necessary information is available (created groups) is the problem of the [Cognitive Dimension](http://blog.architexa.com/2010/04/improving-usability-with-cognitive-dimensions/) Premature Commitment. If you have ever taken an online survey you have probably encountered this problem. Many surveys consist of multiple pages; users are often unaware of the type and number of questions that will be asked. Showing the user the number of total pages and their corresponding headers will allow users to confidently add or modify content during the current phase without having to backtrack. Premature commitment causes problems with all types of actions performed by users; whether it is the creation, modification, or exploration of content. It should be avoided at all costs.
  
<!--more-->


  
Another example for developers is the premature commitment inherent in designing databases. We have all had to choose an initial database structure and then go back and modify it to incorporate changes to the software&#8217;s specification or unexpected types of data. Choosing table and fields names makes perfect sense until you realize that the world is full of exceptions to the rules you put in place. One way to counter this particular example would be to make modifying the database as easy as changing the font in your word processor. This would reduce the [Viscosity](http://blog.architexa.com/2010/05/cognitive-dimensions-viscosity/) present in the database editing tools.

Care is needed when determining what order user actions take place in. The designer&#8217;s expectations often differ from the users. Differences between these expectations can lead to Premature Commitment frustration on the user’s side. Significant usability testing is one way to get around the preconceptions of designers and developers. For most domains it is nearly impossible to eliminate Premature Commitment all together but taking it into account when making design decisions will make your software&#8217;s forms much easier to use.

<small>photo credit: <a href="http://www.flickr.com/photos/20993292@N08/2232897539/">flickr</a></small>

<div style="clear:both;">
  &nbsp;
</div>