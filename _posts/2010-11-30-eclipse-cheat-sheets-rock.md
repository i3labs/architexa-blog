---
id: 183
title: Eclipse Cheat Sheets Rock
date: 2010-11-30T11:18:42+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=183
permalink: /2010/11/eclipse-cheat-sheets-rock/
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

[<img class="alignright size-medium wp-image-190" title="Cheating" src="assets/uploads/2010/11/Cheating1-300x200.jpg" alt="" width="300" height="200" srcset="assets/uploads/2010/11/Cheating1-300x200.jpg 300w, assets/uploads/2010/11/Cheating1.jpg 336w" sizes="(max-width: 300px) 100vw, 300px" />](assets/uploads/2010/11/Cheating1.jpg)The hardest part in creating a user interface or complex feature is explaining to the user how it should be used. No matter how useful a feature is, if users can not figure out how to use it, it won’t provide them any benefit.

Tutorials and wizards can both help in getting users easily using features for the first time. Tutorials can be good at describing the steps necessary to perform a task where users may want to modify the steps in order to accommodate their specific needs. But tutorials do not typically live within your plugin/product and force users to switch between a tutorial on a website and your product. Wizards are great for taking a user through an ordered series of configuration actions but they also have their weaknesses. Wizards live entirely in a dialog box, which not only has to be designed by the development team, but also does not provide nearly enough flexibility. This is where a little known feature of Eclipse comes to the rescue.

<!--more-->

<div style="width: 271px" class="wp-caption alignleft">
  <img title="cheatsheetStart" src="assets/uploads/2010/11/cheatsheetStart.png" alt="" width="261" height="586" />
  
  <p class="wp-caption-text">
    An example of a cheat sheet. This happens to be the cheat sheet for creating an Eclipse Plugin
  </p>
</div>

**Eclipse addresses the problems with tutorials and wizards by combining their best parts to create the concept of &#8216;Cheat Sheets.&#8217;** A cheat sheet allows you to guide a user through a set of ordered instructions much like a traditional wizard, except that the steps are taken directly within the Eclipse IDE instead of a dialog box. Cheat sheets use a simple XML format, so they&#8217;re easily modified and updated just like an online tutorial. Because they are integrated in the IDE users will not have to remember instructions or continuously switch between a website and their workspace. Cheat sheets also contain many useful features such as: collapsible steps that allow you to quickly switch between tasks or backtrack, a UI that can move into opened dialog boxes so it is never obscured, and compound cheat sheets that combine multiple groups of tasks into one.

If you&#8217;ve never used an Eclipse Cheat Sheet before the first thing you should do is try out one of the built in ones. You can find them in Eclipse by going to &#8216;Help&#8217; -> &#8216;Cheat Sheets.&#8217;  You can then select one such as &#8216;Java Development&#8217; -> Create a Hello World Application. You can also select one from a file or URL. Following the instructions in the cheat sheet view that pops up will give you a good idea of the process and what your plugin specific cheat sheet should include.

For us one of the problems we encountered was that users were not sure what to do with the <a href="http://www.architexa.com" target="_blank">Architexa</a> tool once they got it up and running. There was no clear starting point and users were getting lost. We solved this issue by using cheat sheets to compliment the initial user experience. When users activate our client for the first time we automatically open a composite cheat sheet, walking users through the initial steps in creating a diagram. This gives users a clear place to start and helps them to get their hands dirty right away.

Using cheat sheets is easy. They are flexible, can be easily updated, can be posted online, and provide the benefits of both a tutorial and a wizard all within the Eclipse IDE.  Even if you are not building a plugin for Eclipse, the concept of cheat sheets can be implemented in other products. Word processors, spreadsheets, cloud apps, and even other IDEs could benefit from cheat sheets. Upcoming posts will guide you through creating your own cheatsheets, giving you tips and specific examples. If you are already using cheat sheets with your plugin, let us know if you have any specific tips and tricks, or if there is a specific topic you would like covered in more depth.

<div style="clear:both;">
  &nbsp;
</div>