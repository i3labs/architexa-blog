---
id: 125
title: 'High Level Documentation: Layered or Package Diagrams?'
date: 2010-08-23T17:40:01+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=125
permalink: /2010/08/high-level-documentation-layered-or-package/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'UML &amp; Diagramming'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-medium wp-image-129" title="strata" src="{{site.baseurl}}/assets/uploads/2010/08/strata-300x198.jpg" alt="Layers or packages?" width="300" height="198" srcset="{{site.baseurl}}/assets/uploads/2010/08/strata-300x198.jpg 300w, {{site.baseurl}}/assets/uploads/2010/08/strata.jpg 472w" sizes="(max-width: 300px) 100vw, 300px" />]({{site.baseurl}}/assets/uploads/2010/08/strata.jpg)Layered diagrams seem to have become an integral part of <a href="http://www.architexa.com/" target="_blank">documenting code</a> well, but many developers don&#8217;t realize that they aren&#8217;t technically included in the UML spec. The UML standard provides a different sort of high level concept: the Package Diagram. It is often not clear when one should be used over the other, but I will attempt to show the strengths and weaknesses of both.

<p style="text-align: left;">
  A layered diagram is useful for organizing and understanding the structure of a large code base from the top most level down. Instead  of using cumbersome directory trees or code searches to determine the relationships between packages, you can easily see them all in one space. Someone unfamiliar with the code base can easily examine a layered diagram and in a short time will have a grasp of the dependencies inherent in the project without having to be bogged down with details on classes or methods. It is also possible to include architectural components in a layered diagram, including databases, cloud/web components, and UIs. This allows for a flexible diagram that can show a great deal of information concisely.A project with a complex but easily understandable layered diagram is a sign of a well organized codebase.
</p>

<p style="text-align: left;">
  <!--more-->
</p>

<div id="attachment_128" style="width: 310px" class="wp-caption aligncenter">
  <a href="{{site.baseurl}}/assets/uploads/2010/08/layers.png"><img class="size-medium wp-image-128" title="layers" src="{{site.baseurl}}/assets/uploads/2010/08/layers-300x225.png" alt="Layered Diagram" width="300" height="225" srcset="{{site.baseurl}}/assets/uploads/2010/08/layers-300x225.png 300w, {{site.baseurl}}/assets/uploads/2010/08/layers.png 790w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    Here we see a Layered Diagram showing the architecture and relationship of multiple packages by grouping them in layers
  </p>
</div>

However not all layered diagrams are created equal. Small projects do not have much use for layered diagrams since the dependencies involved are often immediately obvious. Other projects where packages are poorly named or organized in an unintuitive way will have equally uninformative diagrams. (Although these diagrams might still be less confusing than studying the codebase to determine what is going on). Layered diagrams also do not provide the fine grain detail needed when working on a specific feature or class.

Overall, a properly created layered diagram is a tool most useful for understanding large code bases and finding hidden dependencies and should not be relied on too heavily when looking at the details of a project.

While layered diagrams group packages based on various abstractions and hierarchies, package diagrams show a high level view of a project by displaying named file folder icons connected by lines representing dependencies between packages. This may at first seem much less powerful but package diagrams can be adapted to highlight the structure of many different types of elements such as classes, use cases, and data entities.

Incorporating packages and package diagrams with other diagram types can allow you to describe a process from a higher level and simplify your diagrams. For example creating a use case diagram for a complex highly interactive project with many components can become overwhelming and convoluted. Grouping similar use cases into logical packages can make the diagram more accessible and provide a possible starting point for organizing your code base.

<p style="text-align: left;">
  Large projects may need a detailed organizational plan. Package diagrams are perfect for this task. Using each package to represent groups of sub-packages allows a software architect to model the package structure with great detail and understand exactly how packages depend on each other. Layered diagrams are often also used for this task. In this case using both types in conjunction can help to illuminate problem areas.
</p>

<p style="text-align: left;">
  <div id="attachment_127" style="width: 310px" class="wp-caption aligncenter">
    <a href="{{site.baseurl}}/assets/uploads/2010/08/Package_Diagram.png"><img class="size-medium wp-image-127 " title="Package_Diagram" src="{{site.baseurl}}/assets/uploads/2010/08/Package_Diagram-300x179.png" alt="Package Diagram" width="300" height="179" srcset="{{site.baseurl}}/assets/uploads/2010/08/Package_Diagram-300x179.png 300w, {{site.baseurl}}/assets/uploads/2010/08/Package_Diagram-1024x614.png 1024w, {{site.baseurl}}/assets/uploads/2010/08/Package_Diagram.png 1429w" sizes="(max-width: 300px) 100vw, 300px" /></a>
    
    <p class="wp-caption-text">
      Here is a package diagram highlighting the high level relationships and usecases between different packages in a medical/search project.
    </p>
  </div>
  
  <p style="text-align: left;">
    In general, layered diagrams are best used when showing the conceptual structure of the package hierarchy quickly and concisely. Package diagrams are best used when grouping other UML diagrams and showing their relationships to the overall package structure. Both are well suited to organizing and designing a large codebase especially when working in an agile environment where architectural changes are an inevitability.
  </p>
  
  <div style="clear:both;">
    &nbsp;
  </div>