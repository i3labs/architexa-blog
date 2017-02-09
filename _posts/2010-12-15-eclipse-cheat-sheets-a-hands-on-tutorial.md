---
id: 184
title: 'Eclipse Cheat Sheets: A Hands on Tutorial'
date: 2010-12-15T17:41:47+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=184
permalink: /2010/12/eclipse-cheat-sheets-a-hands-on-tutorial/
wpbb_sync_comments:
  - 'yes'
categories:
  - Developer Tools
  - Java
tags:
  - Cheat Sheets
  - eclipse
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img src="assets/uploads/2010/11/Cheating1-300x200.jpg" alt="" title="Cheating" width="300" height="200" class="alignright size-medium wp-image-190" srcset="assets/uploads/2010/11/Cheating1-300x200.jpg 300w, assets/uploads/2010/11/Cheating1.jpg 336w" sizes="(max-width: 300px) 100vw, 300px" />](assets/uploads/2010/11/Cheating1.jpg)
  
Based on the great response we have had to our previous cheat sheets articles, ([why they rock](http://blog.architexa.com/2010/11/eclipse-cheat-sheets-rock/) and [tips and tricks](http://blog.architexa.com/2010/12/eclipse-cheat-sheets-tips-and-tricks/)), I have decided to post a more in depth tutorial. One of the many benefits of Cheat sheets is that they provide an immediate improvement to your product’s usability and are simple to implement. This article will allow you to quickly create multiple cheat sheets. 

To help get you started we have created a **cheat sheet on cheat sheets**: This cheat sheet can be opened from within eclipse and will guide you through the simple steps for setting up a cheat sheet for your own project.
  
<!--more-->


  
To use our Cheat Sheet cheat sheet simply open Eclipse. go to ‘Help ->Cheat Sheets..’ and choose ‘Enter the URL of a cheat sheet.’ Enter the following url in the box provided:
  
<code style="font-weight:bold;">&lt;b>http://www.architexa.com/downloads/CheatSheetExample.xml&lt;/b></code>

### Steps for creating a cheat sheet for an Eclipse Plugin

1. In your project&#8217;s plugin.xml file, add the cheat sheet extension point under the Extensions tab: org.eclipse.ui.cheatsheets.cheatSheetContent

2. You can group the cheatsheets you create into categories. These categories are what appear as the folders in Help > Cheatsheets. To create a category, right click the cheat sheet extension point and add a &#8216;New > category&#8217;. Give the category an id and a name. If you don&#8217;t create a category, your cheatsheets will just go into an &#8220;Other&#8221; category.

3. Right click the extension again and choose &#8216;New > cheatsheet&#8217;. Again specify an id and name and also put the category that we just created.

4. Notice you need to specify the cheatsheet&#8217;s content file. This will be an XML file of the instructions shown to the user.

### Creating a cheat sheet content file

The xml structure for a cheat sheet is simple and intuitive. Knowing what you want to accomplish and what options are available to you are the most important parts. Learning by example is the simplest solution. I have compiled a list of the tags you will most commonly use and their function

An _<item>_ is one top-level step in a cheat sheet. Its title is shown all the time; the description is shown when the step is being executed. It can contain _<action>_, _<command>_, or _<perform-when>_ elements that the user presses to perform the step&#8217;s instruction instead of doing it manually. If no action or command is present, the user is required to do it manually and then indicate they completed it by clicking a &#8220;Click when complete&#8221; button.

An item can contain _<subitem>_ elements, which describe a sub-step in a cheat sheet. A _<conditional-subitem>_ describes a sub-step that can differ based on a condition such as a value at the time the item is expanded of a variable set in an earlier step. A _<repeated-subitem>_ allows a step to include a set of similar sub-steps. See the list of tags below for details and other useful tags.

<fieldset>
  <legend>Cheat Sheet Tags:</legend> 
  
  <ul>
    <li>
      <em>intro</em>: What&#8217;s shown before the task is started
    </li>
    <li>
      <em>description</em>: block of descriptive text for an item or intro. Can include simple HTML tags
    </li>
    <li>
      <em>item</em>: A top level step in the cheat sheet. It has a property &#8216;title&#8217; which is the name of the step. It can contain the following: <ul>
        <li>
          <em>subItem</em>: A substep for this item. Can also contain any tag an item contains
        </li>
        <li>
          <em>description</em>: block of descriptive text
        </li>
        <li>
          <em>command</em>: allows you to run a command from within the cheat sheet.
        </li>
        <li>
          <em>action</em>: allows you to run an action from within the cheat sheet.
        </li>
        <li>
          <em>perform-when</em>: allows you to run a command or action when a certain condition is met
        </li>
        <li>
          <em>conditional-subitem</em>: allows you to add a subitem based on the previous state of the cheat sheet
        </li>
        <li>
          <em>repeated-subitem</em>: allows you to add multiple subitems in a variable loop
        </li>
      </ul>
    </li>
  </ul>
</fieldset>

Here is an example of the common tags in action: 

 `<?xml version="1.0" encoding="UTF-8"?><br />
<cheatsheet title="Getting started with MyPlugin"><br />
<intro><br />
<description><br />
Welcome to the tutorial.  Let's get started!<br />
</description><br />
</intro><br />
<item title="Enter a title for your first task here" ><br />
<description><br />
Include some explanatory text here or list some instructional walkthrough steps.<br />
1. Step 1..<br/><br/><br />
2. Step 2..<br/><br/><br />
</description><br />
</item><br />
<item title="Enter a title for your second task here" ><br />
<description><br />
More explanatory text or instructional steps here..<br />
</description><br />
</item><br />
<item title="Open the view from a conditional subitem"><br />
<description>Open a view depending on a variable that has been set.</description><br />
<conditional-subitem condition="${result}"><br />
<subitem when="Package Explorer" label="Open package explorer."><br />
<command serialization = "org.eclipse.jdt.ui.PackageExplorer"/><br />
</subitem><br />
<subitem when="Search View" label="Open Search View"><br />
<command serialization = "org.eclipse.search.ui.views.SearchView"/><br />
</subitem><br />
</conditional-subitem><br />
</item><br />
</cheatsheet><br />
` 

### Composite cheatsheets

If you would like to have a composite cheatsheet that manages a set of related tasks, set the composite attribute to true. Composite cheatsheets have a different XML schema for their content files.

<fieldset>
  <legend>Composite Cheat Sheet Tags:</legend> 
  
  <ul>
    <li>
      <em>taskGroup</em>: As stated, a composite cheatsheet manages a set of related tasks. A &#8220;task group&#8221; represents a collection of related tasks.
    </li>
    <li>
      <em>task</em>: A task represents a single sub-cheatsheet that makes a section of the composite
    </li>
    <li>
      <em>onCompletion</em>: Displayed in the completion panel, which appears once all the <em>items</em> in a cheatsheet are completed.
    </li>
    <li>
      <em>kind</em> a property of task groups that specifies how the user must complete them and can be one of &#8220;set&#8221;, &#8220;sequence&#8221;, or &#8220;choice&#8221;. <ul>
        <li>
          <em>Set</em>: All children tasks must be completed
        </li>
        <li>
          <em>Sequence</em>: All children tasks must be completed and in order
        </li>
        <li>
          <em>Choice</em>: Complete when any child task is completed
        </li>
      </ul>
    </li>
    
    <li>
      <em>skip</em>: A property of tasks, if set to true the task or group of tasks can be skipped
    </li>
  </ul>
</fieldset>

An example of a composite cheat sheet:
  
`<br />
<?xml version="1.0" encoding="UTF-8"?><br />
<compositeCheatsheet<br />
name="Getting started with Architexa"><br />
<taskGroup name="Getting started with Architexa" kind="set"><br />
<intro><br />
Welcome!<br />
</intro><br />
<onCompletion><br />
Great! You have completed the tutorial!<br />
</onCompletion><br />
<task<br />
kind="cheatsheet" name="Using Layered Diagrams"<br />
id="createLayeredDiagram"><br />
<param name="id" value="com.architexa.diagrams.all.ui.layeredCheatSheet" /><br />
<param name="showIntro" value="true" /><br />
<intro><br />
This tutorial guides you through the creation of a Layered Diagram.<br />
</intro><br />
<onCompletion><br />
Finished creating a Layered Diagram.<br />
</onCompletion><br />
</task><br />
<task .... more tasks...<br />
</taskGroup><br />
</compositeCheatsheet><br />
` 

### Opening Cheat Sheets Programmatically

In many cases you may want to make your cheat sheets more accessible to the user. They can be included in wizards, help buttons/links, or anywhere else in your plugin. To launch a cheat sheet automatically create a new OpenCheatSheetAction instance with the parameter equal to the id of the desired cheat sheet as defined in the xml file. Running this action will open the cheat sheet.

### More Information

For more information on these tags, additional properties, and specific information on their usage see the below references:

  * [Eclipse SDK Help](http://help.eclipse.org/helios/index.jsp?topic=/org.eclipse.platform.doc.isv/guide/ua_cheatsheet.htm)
  * [Oracle: Building Cheat Sheets in Eclipse](http://www.oracle.com/technetwork/articles/entarch/eclipse-cheat-sheets-092351.html)

<div style="clear:both;">
  &nbsp;
</div>