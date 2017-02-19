---
id: 82
title: Commands and the MVC architecture
date: 2010-06-12T20:34:11+00:00
author: Abhishek Rakshit
layout: post
guid: http://blog.architexa.com/?p=82
permalink: /2010/06/commands-and-the-mvc-architecture/
categories:
  - 'Design Patterns &amp; Architecture'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-full wp-image-85" title="Commands and MVC" src="{{site.baseurl}}/assets/uploads/2010/06/ctrlZ2.jpg" alt="" width="243" height="217" srcset="{{site.baseurl}}/assets/uploads/2010/06/ctrlZ2.jpg 405w, {{site.baseurl}}/assets/uploads/2010/06/ctrlZ2-300x268.jpg 300w" sizes="(max-width: 243px) 100vw, 243px" />]({{site.baseurl}}/assets/uploads/2010/06/ctrlZ2.jpg)Most of us agree to the benefits of using commands to provide the undo-redo functionality in an <a href="http://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller" target="_blank">MVC</a> based application. Working on one such highly interactive application, the question which often arises is **where in the code base do the commands belong**: in the model, in the controller or as a separate entity. This issue has been discussed before and people seem to have quite disparate views implying a vague understanding of this problem. In my view commands should be considered separate from both the model as well as the controller. This becomes really important while organizing your code to have clear abstraction boundaries and conform with the principles of <a href="http://blog.architexa.com/2010/06/cohesion-and-coupling-in-large-projects/" target="_blank">cohesion and coupling</a>. <!--more-->

As per convention, in an MVC architecture models depend on neither the view nor the controller. Similarly, commands are also always independent of the view or the controller. Moreover, in some cases business logic related to the modification of models is also present in commands. These characteristics might suggest that commands should be in the model domain.

On the other hand, traditionally controllers are responsible for handling the request from the view and to call the appropriate methods on the model. Commands take over the controllers responsibilities of routing the request to the model, and all the controller has to do is call an execute on the command. These facts may give an inkling that commands are related to the controller domain.

Commands due to their similarities with both the model and the controller, fall into a grey area raising ambiguity around their placement in the code. If we take a look at the underlying nature of the commands, they add another layer of abstraction due to which the controller does not have to worry about knowing how the models get updated. Every command works only on a specific type of element and is responsible for a specific task with respect to the model. So basically it a feature which encapsulates the code to appropriately modify the models on request of the controller.

Placing commands separately from the model as well as the controller has many benefits. Commands if added to the controller&#8217;s domain make the controller bulky and also increases the chance of unintentionally moving more controller responsibilities into the command. On the other hand we risk adding unnecessary model related business logic in the commands if they reside in the model domain. Commands for the most part have come into existence for the specific purpose of providing undo-redo functionality. This specific nature in itself suggest them to be a distinct entity. Separating out the commands forces us to have a clear understanding of the functional boundaries of all the the three components. This not only helps is keep our code base clean but also, our applications become more manageable in terms of scaling as well as testing.

<div style="clear:both;">
  &nbsp;
</div>