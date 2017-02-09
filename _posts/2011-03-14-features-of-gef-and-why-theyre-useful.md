---
id: 236
title: 'Features of GEF and why they&#8217;re useful'
date: 2011-03-14T18:59:05+00:00
author: seth
excerpt: |
  GEF provides a great framework for building MVC based plugins on the Eclipse platform. It contains a great deal of the core functionality (described in more detail <a href="http://blog.architexa.com/2011/03/a-simple-intro-to-creating-a-mvc-framework-using-gef/">here</a>)  necessary for building these types of apps. In addition, GEF also provides features that greatly simplify the task of creating a robust interactive editor. I'll try to show how these different features can benefit any Eclipse developer working with GEF.
layout: post
guid: http://blog.architexa.com/?p=236
permalink: /2011/03/features-of-gef-and-why-theyre-useful/
wpbb_sync_comments:
  - 'yes'
categories:
  - Eclipse
  - Java
tags:
  - eclipse
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img src="/assets/uploads/2011/03/logo-300x69.jpg" alt="" title="logo" width="300" height="69" class="alignright size-medium wp-image-229" srcset="/assets/uploads/2011/03/logo-300x69.jpg 300w, /assets/uploads/2011/03/logo.jpg 499w" sizes="(max-width: 300px) 100vw, 300px" />](/assets/uploads/2011/03/logo.jpg)GEF provides a great framework for building MVC based plugins on the Eclipse platform. It contains a great deal of the core functionality (described in more detail [here](http://blog.architexa.com/2011/03/a-simple-intro-to-creating-a-mvc-framework-using-gef/))  necessary for building these types of apps. In addition, GEF also provides features that greatly simplify the task of creating a robust interactive editor. I&#8217;ll try to show how these different features can benefit any Eclipse developer working with GEF.<!--more-->

**Tools**
  
Tools allow you to change how users can interact with the editor. For example, when using a paint program the paint brush, eraser, and crop actions are all tools. You can also use them to do specific tasks such as creating new objects, dragging, or resizing depending on which tool is selected. Tools can be a powerful addition to a complex editor giving the user finer control, but it can also result in the interface becoming unintuitive if used in the wrong situation. Sometimes you may want to simplify the UI intelligently by guessing which task the user is attempting by where and how they are clicking. For instance, instead of adding a tool for resizing an element, you could check if the user is selecting/dragging the edge of an element and then change the command that is generated to the appropriate resize command.

**Editpolicies**

Editpolicies help you to separate the logic of getting commands from requests into a separate class. This Editpolicy class can be used by any number of editparts that utilize similar actions. For example, many editparts will have the same logic when for creating a move command. Editpolicies can also be used to abstract other editpart responsibilities such as management of the visual feedback shown to the user while editing, moving, or dragging an item.

  
<span>View more <a target='_blank' href='http://www.codemaps.org'>Architectural Documentation</a> on <a target='_blank' href='http://www.codemaps.org/s/Eclipse_GEF__API'>Eclipse GEF: API</a> </span>

**Commands and Command Stack Management**

GEF helps maintain a list of commands that have been executed so that they can be undone or re-executed.  To take advantage of this you must override the undo() method in the command class. You must then make sure you track the previous state of the model within your command so that the undo method can change it back. By default redo() calls the execute command again, but you can override this too if the command requires different functionality when being executed a second time.

  
<span>View more <a target='_blank' href='http://www.codemaps.org'>Architectural Documentation</a> on <a target='_blank' href='http://www.codemaps.org/s/Eclipse_GEF__API'>Eclipse GEF: API</a> </span>

These are just some of the interesting and useful features in GEF. What are your favorites?

&nbsp;

&nbsp;

<div style="clear:both;">
  &nbsp;
</div>