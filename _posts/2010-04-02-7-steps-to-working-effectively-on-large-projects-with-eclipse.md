---
id: 14
title: 7 steps to working effectively on large projects with Eclipse
date: 2010-04-02T01:23:36+00:00
author: Vineet Sinha
layout: post
guid: http://blog.architexa.com/?p=14
permalink: /2010/04/7-steps-to-working-effectively-on-large-projects-with-eclipse/
categories:
  - Developer Tools
  - Java
tags:
  - eclipse
  - Java
  - large projects
  - tools
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

Large projects often come with an independent (usually ant based) build system &#8211; so that the project can be built effectively in different situations. For programmers working on these projects, this often means setting up the IDE to work with these build systems. While working with development teams, I have seen way too many examples of the IDE not setup to take advantage of some of their features. Especially these days, IDE&#8217;s absolutely rock, so if you are not taking advantage of them then you are likely putting yourself at a disadvantage.

Below are a set of steps that you can follow to configure Eclipse to effectively work on your project:

<!--more-->

**1) Ensure your build system is working**

The first part has nothing to do with your IDE. But before trying to take advantage of all the cool Eclipse features you need to get the basics working first. Depending on the setup, some build systems might need to not only have certain software not running, but also have both the code checked out in particular directories and also have software installed in other fixed directories. Once you have your build system setup, you can configure to use Eclipse with the project.

**2) Project setup in Eclipse**

To setup your project in Eclipse, launch Eclipse and choose a location for the workspace &#8211; the location does not matter as much. Once Eclipse starts go to the <span class="inlineCode">File</span> menu, choose <span class="inlineCode">New</span>, and select <span class="inlineCode">Java Project</span>. Give the project a name, and tell Eclipse to <span class="inlineCode">Create project from existing source</span>, and type in the project directory.

At this point you should be able to edit files from within Eclipse, and have the benefit of having multiple files opened in the various tabs. You can also try <span class="inlineCode">Ctrl+Shift+R</span> to quickly open a file. Eclipse does not yet know about the source code in the project, so you will not see syntax highlighting yet &#8211; for that you will need to get to <span class="inlineCode">step 4</span>.

**3) Using the Build system from within Eclipse**

Now that you have your build system working, you can choose to not have a separate window open for just running the build. Integrating Ant builds into Eclipse is easy &#8211; just find the <span class="inlineCode">build.xml</span>, right click on it, and in the dropdown menu, go to <span class="inlineCode">Run As</span> then <span class="inlineCode">Ant Build</span>. This is the same as doing <span class="inlineCode">ant local</span> &#8211; if you want to run another ant target just click on the <span class="inlineCode">Ant Build&#8230;</span> option instead. The build output will be shown in the Eclipse Console window.

<div>
  <center>
    <img src="assets/uploads/2010/04/findBuildXml.png" alt="Quickly find build.xml using Ctrl+Shift+r" />
  </center>
</div>

Once you have started an ant build you should be able to run it again easily by finding it in the Eclipse toolbar &#8211; look for the green circle containing a white arrow pointing right and having a red suitcase with the text <span class="inlineCode">Run project_name build.xml</span> shown when you hover the mouse over it. Clicking on the drop down should show the various build configurations that you might have created.

<div style="background-color: #dddddd; padding: 5px; margin: 5px;">
  Caution: One common error cause when running ant tasks is when there are multiple ant targets that you want to execute. Make sure that you not only select the ant targets from the configuration dialog but that you also verify that the <span class="inlineCode">Target execution order</span> is correct.
</div>

**4) Using Eclipse&#8217;s Build System**

Once you are able to get the external build system working, you can use Eclipse &#8211; atleast for compiling the Java source files that you modify. On configuring Eclipse, it can not only provide syntax highlighting but also parse any changes even before you save the files so that you can fix code errors immediately. Setting this up means telling Eclipse (a) where your Java code is and (b) where your libraries (jar files) are for building the files.

To configure Eclipse&#8217;s build system, right click on the Project (which you will be able to see in the <span class="inlineCode">Project Explorer</span>, the <span class="inlineCode">Package Explorer</span>, or the <span class="inlineCode">Navigator</span> views) and select <span class="inlineCode">Properties</span>. Once there click on <span class="inlineCode">Java Build Path</span> on the left hand side and to setup your Java code source location make sure that the <span class="inlineCode">Source</span> tab is selected. Here you can add one or more of your folders so that Eclipse can compile them. Next click on the <span class="inlineCode">Libraries</span> tab and add all the jar files that might be needed in the compilation process. Once that is done, hit <span class="inlineCode">OK</span> and let Eclipse build the project. If there are any errors (shown in the <span class="inlineCode">Problems</span> view) then they will need to be fixed.

<div>
  <center>
    <img src="assets/uploads/2010/04/launchBuild.png" alt="run previously created build configurations" />
  </center>
</div>

**5) Debugging in Eclipse**

Beyond having Eclipse help in managing editing code and compiling it, you can also use the great debugger that comes integrated into Eclipse. To do so you would first need to launch your application with remote debugging enabled. The details depend on how you launch the app, but it mostly boils down to starting the JVM with <span class="inlineCode">-Xdebug</span> and <span class="inlineCode">-Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=1044</span> (see [here](http://java.sun.com/j2se/1.4.2/docs/guide/jpda/conninv.html) for jvm launching details).

Once you launch the JVM, you need to create a remote debugging instance from within Eclipse. Go to the main menu, select <span class="inlineCode">Run</span>, choose <span class="inlineCode">Debug Configurations&#8230;</span>, select <span class="inlineCode">Remote Java Application</span> in the left side and click on the <span class="inlineCode">New launch configuration</span> button at the top of the left side. The degug configuration will need a name, and all you need to do is select the project that you will be debugging (so that Eclipse knows where to map the code stepping to), and then to click on the <span class="inlineCode">Apply</span> button. With this configuration setup you should be able to connect to any launched instance by running the debug configuration.

**6) Fixing bugs while debugging&#8230;.**

One of the nice things of modern IDE&#8217;s is that if while debugging and stepping through your Java code you find a bug, you can just edit it and continue executing the code with the new changes. Even while working with an externally launched application you can easily setup Eclipse to do hot code replacements as needed. To do this, all you need to do is have the class files generated by Eclipse&#8217;s builder to be placed in the correct directory. You can change these build settings by right clicking on the project, select <span class="inlineCode">Properties</span>, then <span class="inlineCode">Java Build Path</span> and <span class="inlineCode">Source</span> to make sure the <span class="inlineCode">Default output folder</span> is in the same directory as the external build system is placing the .class files (thus letting Eclipse to take your changes over-write the older class files).

**7) Document integration**

Ok, now that you have gotten Eclipse working well for your project, the next step would be document the steps so that the rest of the team can benefit from your experience. (perhaps you can use this article as a template to start).

<div style="clear:both;">
  &nbsp;
</div>