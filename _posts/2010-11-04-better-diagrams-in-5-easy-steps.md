---
id: 138
title: Better Architectural Documentation in 5 easy steps
date: 2010-11-04T16:11:02+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=138
permalink: /2010/11/better-diagrams-in-5-easy-steps/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Documentation &amp; Communication'
  - 'UML &amp; Diagramming'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright" title="Stairs" src="assets/uploads/2010/11/Stairs-263x300.jpg" alt="" width="210" height="240" />](assets/uploads/2010/11/Stairs.jpg)Documenting code can be a time consuming challenge, especially when dealing with unfamiliar spaghetti code. Diagrams and UML tools can help with this but what appears to be a comprehensive diagram to one person might actually result in more confusion to someone else. It&#8217;s important to maintain a clear idea of what concepts your diagram is conveying. I often find myself attempting to document entirely with inline comments. This is often very useful but presents challenges when documenting concepts that span <span style="font-size: 13.3333px;">multiple classes/methods. There are several tricks I&#8217;ve found that make the task of diagramming code significantly easier.</span>

<!--more-->

**Images cannot survive in a vacuum**
  
Diagrams should not be the only source of documentation for your codebase. Inline comments, javadoc, and architectural guidelines all help compliment diagrammatic documentation. Diagramming tools that allow you to add ordered comments or javadoc directly within the diagram can help ease the burden on documenters by combining corresponding types of documentation in a single image.

**Highlight stumbling blocks**
  
Just like commenting every line of code is not generally a good idea; creating diagrams explaining every nuance of your code should not be your top priority. Diagrams should help show complex or confusing sections of code clearly. Some examples of areas that should be documented are: interesting architectural designs, complex build or layout systems, unique design patterns, complex logic, unintuitive logic or methods, or important exceptions to common use cases. These types of scenarios are often stumbling blocks for new developers. Having diagrams available helps to prevent uninitiated developers from accidentally introducing bugs to key sections.

**Organization is key**
  
Diagrams are useless if they are not readily available to all members of the team. Diagrams should be as easily shared between developers as the code they are working on. This way there is less of a chance of misunderstanding code concepts and everyone is guaranteed to be on the same page. Diagrams can be shared by checking them into the corresponding source repository or using a server to host the diagrams to the entire team. Make sure to also keep diagrams organized in a way that makes sense for your project; grouping by package, component, or level of detail are all excellent methods.

**Keep Updating your diagrams**
  
Diagrams should receive routine maintenance to ensure they are up to date. Old diagrams become progressively less helpful as the underlying code changes more and more. It is helpful to schedule updates every month or so and even more often for code that changes more frequently or in agile environments. Utilizing diagramming tools that detect changes in your code and allow for easy saving and updating makes maintenance significantly easier.

**Less is more**
  
A diagram containing too many components does not necessarily convey more information. More classes, methods, and connections often result in a cluttered diagram that is too convoluted to understand at a glance. However, a concise diagram created within a clearly defined scope and describing a key code concept will much more effectively make even the most complex code easy to understand. Large sprawling diagrams can often be broken down into sub-concepts and organized to provide a fuller, more complete picture.

<div id="attachment_153" style="width: 310px" class="wp-caption aligncenter">
  <a href="assets/uploads/2010/11/log4j.png"><img class="size-medium wp-image-153 " title="log4j" src="assets/uploads/2010/11/log4j-300x126.png" alt="http://www.codemaps.org/groups/pJt2opXWGD9Q/fragments/BDjg0lOkFJZd" width="300" height="126" srcset="assets/uploads/2010/11/log4j-300x126.png 300w, assets/uploads/2010/11/log4j-1024x431.png 1024w, assets/uploads/2010/11/log4j.png 1363w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    This diagram highlights the concept of nested logging messages in apache Log4J. Notice how comments are used in conjunction with specific classes and methods to highlight the important logic.
  </p>
</div>

**(BONUS) Multiple versions**
  
Keep copies of older versions of your diagrams. This helps new developers better understand how the code has evolved and may help illuminate hidden pitfalls or allow others to avoid making the same mistakes. It is also helpful to keep separate versions of your documentation for both unexperienced developers and those familiar with the codebase. Such targeted documentation will result in much quicker understanding for any developer.

<div style="clear:both;">
  &nbsp;
</div>