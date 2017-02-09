---
id: 225
title: 'A simple intro to creating a MVC framework: Using GEF'
date: 2011-04-10T19:28:23+00:00
author: Abhishek Rakshit
layout: post
guid: http://blog.architexa.com/?p=225
permalink: /2011/04/a-simple-intro-to-creating-a-mvc-framework-using-gef/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Design Patterns &amp; Architecture'
  - Eclipse
  - Java
  - 'Libraries &amp; Frameworks'
tags:
  - eclipse
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img src="assets/uploads/2011/03/logo-300x69.jpg" alt="" title="logo" width="300" height="69" class="alignright size-medium wp-image-229" srcset="assets/uploads/2011/03/logo-300x69.jpg 300w, assets/uploads/2011/03/logo.jpg 499w" sizes="(max-width: 300px) 100vw, 300px" />](assets/uploads/2011/03/logo.jpg)When creating a rich graphical editor the Model View Controller (MVC) design pattern makes life a lot easier. But it is often difficult to decide which libraries/frameworks to use. On the Eclipse platform GEF (Graphical Editing Framework) is a great solution but it can be challenging to figure out how to integrate with the parts you need. Since GEF is built on top of the Draw2d/SWT graphical libraries and is able to provide a powerful and consistent UI. However there are many considerations and pitfalls to take into account when getting started with GEF.

Some of my first large scale Java coding involved using and modifying GEF code. Luckily the GEF team provides many helpful examples showcasing the different features GEF offers. I will attempt to provide a concise introduction to the points that I found best helped me understand GEF.
  
<!--more-->

**MVC and GEF**

<div style="margin: 2px; border: 1px solid #ccc; float: right;">
  <br /><span>View more <a target='_blank' href='http://www.codemaps.org'>Architectural Documentation</a> on <a target='_blank' href='http://www.codemaps.org/s/Eclipse_GEF__API'>Eclipse GEF: API</a> </span>
</div>

The Model, View, Controller architecture may seem overly complex at first but it provides many benefits. It allows you to easily decouple the Model your program stores (Database, save files, memory structure, etc) from the view it displays to the user. This allows you to make your code more portable and easier to maintain and update.

GEF also creates an easy to use framework for managing the Controller, this is one of the more complicated concepts in MVC since it connects changes made in the model to corresponding figures in the view. GEF&#8217;s EditParts form the backbone of this framework. EditParts are supplemented by tools, palette, EditPolicies and commands, all of which help communicate actions from the keyboard and mouse to changes in the model and view.

One of the concepts that best helped me get an overview of how GEF implements the MVC architecture was one that explained the details of how a user&#8217;s actions result in changes to both the model and the view. There is a simple flow that begins whenever an action occurs. It traverses the MVC architecture via multiple different design patterns in the following order:

  1. The user acts on the view via the keyboard or mouse.
  2. GEF&#8217;s EditPartViewer determines what tool is being used and fires the appropriate request.
  3. The EditParts determine if they can create a corresponding command for that request
  4. The command is added to the command stack and executed, modifying the model
  5. The model fires the appropriate property change events after it has been modified
  6. EditParts update depending on what property changes are triggered. (For instance a new instance of a model element will trigger the EditPart Factory to instantiate a new corresponding EditPart)
  7. The EditParts update the view according to their new state.
  8. Luckily this whole process is handled by the GEF infrastructure. By creating/extending instances of the GraphicalEditorPartWithPalette, Commands, and EditPolicies you can create a the core of a GEF/MVC application.

**Tips and some mistakes to avoid**
  
I&#8217;ve found a few key concepts that are really helpful to keep in mind while developing with GEF:

_Keep your EditParts out of your commands_
  
In GEF Commands are created by EditParts/EditPolicies based on the Requests sent from user actions. They are responsible for updating the model. Ideally they should be simple atomic changes such as changing an elements size, location, color, or adding a child element. GEF provides CompoundCommands to allow you to combine these tasks into more complex commands. Just be careful to keep your EditParts out of your commands. Any logic requiring the EditPart (such as location of the request) should be handled within the getCommand() method in the EditPart and not within the command.

_Don&#8217;t let your model get chatty with the view_
  
The model should never directly modify the view. Any changes made on the model side should result in property changes being fired and then handled by the EditParts. They are then responsible for making changes to the figures.

_Anything you want to save should be in the model_
  
If there is some information you intend on saving it should be stored in the model. For instance if you intend on tracking where your data objects are in relation to eachother within the view, their coordinates will need to be saved in the model.

_Balance the ratio of model -> controller -> view_
  
You do not necessarily need exactly one EditPart for each model element or one figure for each EditPart. In fact this can lead to many problems. You want to make sure the hierarchy of the model view and controller all make sense within their own domains. After this you can decide how the mapping should work.

<div style="text-align:center;">
  <div style="margin: 2px; border: 1px solid #ccc; width:410px;">
    <br /><span>View more <a target='_blank' href='http://www.codemaps.org'>Architectural Documentation</a> on <a target='_blank' href='http://www.codemaps.org/s/Eclipse_GEF__API'>Eclipse GEF: API</a> </span>
  </div>
</div>

**Other great GEF resources:**

  * GEF Description &#8211; <http://wiki.eclipse.org/GEF_Description>
  * Eclipse GEF Project Page (Download) &#8211; <http://www.eclipse.org/gef/gef_mvc/index.php>
  * GEF Tutorials &#8211; <http://www.eclipse.org/gef/reference/articles.html>
  * Draw2d Tutorial &#8211; <http://eclipse.org/articles/Article-GEF-Draw2d/GEF-Draw2d.html>

<div style="clear:both;">
  &nbsp;
</div>