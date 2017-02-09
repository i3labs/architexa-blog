---
id: 24
title: Determining Which UML Diagram to Use
date: 2010-04-22T16:20:29+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=24
permalink: /2010/04/determining-which-uml-diagram-to-use/
categories:
  - 'UML &amp; Diagramming'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

There are many types of <a href="http://www.agilemodeling.com/essays/umlDiagrams.htm" target="_blank">UML diagrams</a> other than the commonly used class diagram. Choosing between them can be a challenge; which type should we use<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/UML_Diagrams.jpg"><img class="size-medium wp-image-25 alignright" title="UML_Diagrams" src="assets/uploads/2010/04/UML_Diagrams-300x225.jpg" alt="Diagram Collage" width="300" height="225" srcset="assets/uploads/2010/04/UML_Diagrams-300x225.jpg 300w, assets/uploads/2010/04/UML_Diagrams.jpg 420w" sizes="(max-width: 300px) 100vw, 300px" /></a> and when? What diagram is right for my problem/codebase? We&#8217;ve seen that UML Diagrams are great for designing code but how can we make sure they remain useful when maintaining that same code? I spent some time thinking about these questions and here are some of the answers that I have come up with.

#### Structure Diagrams

One type of diagrams are the &#8216;structure diagrams&#8217;, they depict information without regard for temporal ordering. They can help to break large projects or features into parts and specify which parts do what and how they interact. The most common example, <a href="http://en.wikipedia.org/wiki/Class_diagram" target="_blank">Class diagrams</a> <small>(<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/classUML.png">example</a>)</small> are very useful, however there are many more underutilized structure diagrams that can help with specific tasks.
  
<!--more-->

If you are working with a large team and need to break a project into many components you are going to need a <a href="http://en.wikipedia.org/wiki/Component_diagram" target="_blank">Component Diagram</a> <small>(<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/Component-4.png">example</a>)</small>. Combining different parts of your project from different groups of developers becomes much easier with a Component Diagram.

Projects with many different use cases requiring communication between many classes can benefit greatly from <a href="http://en.wikipedia.org/wiki/Composite_structure_diagram" target="_blank">Composite Structure Diagrams</a> <small>(<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/Composite_Structure_Diagram.png">example</a>)</small>. These show how various components collaborate at run-time and are best used to describe how different classes interact during a complex user action. They combine the usefulness of Use Case Diagrams and Sequence Diagrams.

If you have a large codebase with lots of dependencies <a href="http://en.wikipedia.org/wiki/Package_diagram" target="_blank">Package Diagrams</a> <small>(<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/Package_import-1.png">example</a>)</small> help you get a high level overview quickly and easily. They will immediately unveil what dependencies your project has.

Many client-server projects that use a multitude of frameworks, languages, and hardware should use <a href="http://en.wikipedia.org/wiki/Deployment_diagram" target="_blank">Deployment Diagrams</a> <small>(<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/UML_Diagramme_Deploiement.gif">example</a>)</small> if they are not already. Typical J2EE projects can often benefit from such diagrams. Deployment Diagrams provide a useful way to visualize the structure of projects spanning many different hardware environments. A project utilizing a cloud server, multiple databases, and a local machine would benefit from a deployment diagram detailing what software runs where and how it communicates.

#### Behavior Diagrams

When you are dealing with project complexity regarding the actions, behavior, and order in which events occur within your program then you should be using one of the Behavior Diagrams.

Understanding the logic of a specific process, portion of code, or other interaction can be simplified with an <a href="http://en.wikipedia.org/wiki/Activity_diagram" target="_blank">Activity Diagram</a> <small>(<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/678px-Activity_Diagram_1.jpg">example</a>)</small>. Breaking down a process into individual decisions, loops and chains of events helps make many problems easier to understand.  If you are having trouble thinking through a new billing or login process it’s time to break out the Activity Diagram.

If you have a feature where numerous types of users will be using your software in a number of different ways you might need a <a href="http://en.wikipedia.org/wiki/Use_case_diagram" target="_blank">Use Case Diagram</a> <small>(<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/UML_Use_Case_diagram.png">example</a>)</small>. This diagram will help show you a detailed view of how cases and actors are interrelated. Having this information available will help you to determine what actions you will need to support to best accommodate all the users.

#### Interaction Diagrams

Behavior diagrams that emphasize object interactions over time are Interaction Diagrams. Designing a system where there are complex relationships between differing code elements requires a fine grain view of how those elements interact over time.

If you have a project with many concurrent actions and need to determine what order they should occur in you may need a <a href="http://en.wikipedia.org/wiki/Communication_diagram" target="_blank">Collaboration/Communication Diagram</a> <small>(<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/Kommunikations_diagramm-5.png">example</a>)</small>. This very specific diagram type is most important when understanding how and in what order multiple classes interact. Communication diagrams are often ignored in favor of sequence diagrams which are able to show the order of events more clearly.

<a href="http://en.wikipedia.org/wiki/Sequence_diagram" target="_blank">Sequence diagrams</a> <small>(<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/Restaurant-UML-SEQ.gif">example</a>)</small> are for you if you are designing the sequential logic of your project. A properly created sequence diagram will show each method’s calls separated by class instance in the order they were called. This can be very helpful when tracing the execution of a program or determining if a method’s behavior is correct. Sequence diagrams are not all that useful when dealing with asynchronous behavior or complex loops and iterations.

If you find yourself using many Activity Diagrams and want to see how they are related a <a href="http://en.wikipedia.org/wiki/Interaction_overview_diagram" target="_blank">Interaction Overview Diagram</a> <small>(<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/interactionUML-1.png">example</a>)</small> will be helpful. Each node in an Interaction Diagram can represent another complete Activity/Interaction Diagram. This can be very helpful when dealing with nested logic or complex combinations of logic.

A project that contains many objects that frequently change state over a period of time would benefit from a <a href="http://en.wikipedia.org/wiki/Timing_diagram_(Unified_Modeling_Language)" target="_blank">Timing Diagram</a> <small>(<a rel="wp-prettyPhoto" href="assets/uploads/2010/04/example-of-a-timing-diagram.png">example</a>)</small>. Without a such a diagram you may not realize how potential periods of high traffic could intersect and overwhelm your program.

#### Summary

Not every project needs to use every type of UML diagram. Each project presents its own challenges; hopefully now you are well versed in the potential of diagrams as solutions. A well thought out set of correctly chosen diagrams created during the design process of a project can alleviate many headaches later on in the development cycle.

<small>Image credit: <a href="http://en.wikipedia.org/wiki/File:UML_Diagrams.jpg" target="_blank">wikipedia</a></small>

<div style="clear:both;">
  &nbsp;
</div>