---
id: 185
title: 'Eclipse Cheat Sheets: Tips and Tricks'
date: 2010-12-08T17:25:29+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=185
permalink: /2010/12/eclipse-cheat-sheets-tips-and-tricks/
wpbb_sync_comments:
  - 'yes'
categories:
  - Developer Tools
  - Java
tags:
  - eclipse
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[](/assets/uploads/2010/11/Cheating.jpg)[<img class="alignright size-medium wp-image-190" title="Cheating" src="/assets/uploads/2010/11/Cheating1-300x200.jpg" alt="" width="300" height="200" srcset="/assets/uploads/2010/11/Cheating1-300x200.jpg 300w, /assets/uploads/2010/11/Cheating1.jpg 336w" sizes="(max-width: 300px) 100vw, 300px" />](/assets/uploads/2010/11/Cheating1.jpg)We talked about in a previous post why [Cheat Sheets Rock](http://blog.architexa.com/2010/11/eclipse-cheat-sheets-rock/). Our users have found them useful in the [Architexa](http://www.architexa.com) plugin and we are in the process of adding a great deal more cheat sheets to it. We have also had requests from our readers for more details on creating and utilizing cheat sheets effectively. Some of the most important tips that we found helpful while adding cheat sheets to our product are below to help you get started.
  
<!--more-->


  
**Creating Cheat Sheets**

When thinking about the content of your cheat sheet, remember to consider what type of user will be using it. New users will need an overview, introduction, or walkthrough of the main points of your plugin. Familiar users will need instructions on more advanced tasks.

Also make sure to take into account the point of view of the user when choosing a title for your cheat sheet. A user looking for a feature that solves a specific problem will have an easier time finding the appropriate help if the cheat sheet is named for the problem he is having instead of explaining a feature he might not be aware of.

There are some situations where a cheat sheet may not be the best method of documentation. If you want to include lots of screenshots, rich hyper-linked text, or if your described task requires a lot of user inputted text, cheat sheets might not be right for you. Use an Eclipse Help menu or online documentation to more effectively describe these tasks.

If you have a large task to explain or if it can be easily broken into sub-tasks, you may want to use Composite Cheat Sheets. These allow you to combine any number of cheat sheets into one so that a user can step through them in order. This is especially helpful for overview and setup tasks where you want to guide a beginner user through different aspects of your plugin in a specific order.

Some other tips from the [Eclipse Cheat Sheet Best Practices](http://help.eclipse.org/helios/index.jsp?topic=/org.eclipse.platform.doc.isv/guide/ua_cheatsheet_guidelines.htm):

>   * Utilize links to the help system in cheat sheet tasks whenever possible to provide background or more detailed information
>   * Consider rewriting as a composite cheat sheet if there are more than 10 steps.
>   * Utilize commands where possible to perform simple tedious tasks such as opening perspectives, opening resources, executing wizards. Be sure to also provide a description of how to achieve the same effect without using the command.
>   * Ensure commands can be skipped if the user decides to do the steps manually
>   * Specify dialog=&#8221;true&#8221; for steps which open dialogs. This will cause the cheat sheet to open in a &#8220;tray&#8221; to the right of  most dialogs.
>   * Organize the steps in such a way that the user sees visible signs of success frequently. A cheat sheet that makes a number of different changes to java source and then launches an application could be rewritten so that the application was launched after each source change.
>   * [more](http://help.eclipse.org/helios/index.jsp?topic=/org.eclipse.platform.doc.isv/guide/ua_cheatsheet_guidelines.htm)

These are just some tips to get you started. In our next Cheat sheet post, we&#8217;ll be going over and explaining some specific cheat sheet examples.

<div style="clear:both;">
  &nbsp;
</div>