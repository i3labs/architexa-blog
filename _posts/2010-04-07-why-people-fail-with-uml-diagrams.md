---
id: 18
title: Why People Fail With UML Diagrams
date: 2010-04-07T11:04:10+00:00
author: seth
layout: post
guid: http://blog.architexa.com/?p=18
permalink: /2010/04/why-people-fail-with-uml-diagrams/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'UML &amp; Diagramming'
tags:
  - diagrams
  - uml
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

UML and UML tools seem to always be getting a lot of[<img class="alignright size-full wp-image-21" title="uml-top" src="assets/uploads/2010/04/uml-top1.png" alt="UML LOGO" width="106" height="87" />](assets/uploads/2010/04/uml-top1.png) bad press. This might be the result of developers not utilizing them for their intended purposes. As they were originally imagined, <a href="http://en.wikipedia.org/wiki/Unified_Modeling_Language#Diagrams_overview" target="_blank">UML diagrams</a> should _only_ be used when designing code. They should not be used when sitting down to detangle a pile of incomprehensible logic or making sense of an alien design pattern; and especially not for generating all your project&#8217;s code. Experienced designers may already have come to this realization but for others some explanation is in order.

There are a lot of options when it comes to UML diagrams. Other than the ever present Class Diagram there are: Structure Diagrams (class, deployment, package, etc), Behavior Diagrams (activity, usecase, etc), and Interaction Diagrams (communication, sequence, etc). They are all used to meet a very specific need; communicating design requirements from product management to the development team. This is very important when working with most software processes since they require all functionality to be determined during the design phase. Five months later when features are added/removed and code is re-factored, maintaining the UML diagrams becomes tedious and the diagrams are no longer helpful.
  
<!--more-->


  
The strict guidelines governing [UML](http://uml.org/#UML2.0) usage are great for preventing ambiguity during the design process but immediately become a nuisance when a new team member needs to understand how a new feature relates to the existing codebase. Software Architects can take advantage of the power of the UML to create detailed specifications that would be difficult to create with other tools. However, much of the information in UML diagrams is represented by unintuitive, non-graphical symbols. For example, the 1-* notation in class diagrams conveys that a one to many relationship exists but this may not be immediately obvious from a cursory glance at the diagram. In fact, it is often difficult to get a quick overview of a feature or concept since most aspects are broken into separate UML diagrams. Someone new to a large project would have to pour over piles of diagrams to get a clear idea of the task at hand.

Some UML tools are marketed with claims that they can provide unlimited diagramming abilities and solve all your programming problems; allowing you to understand existing code and even generate code. However they often fall short when it comes to keeping diagrams concise or modifying existing diagrams. These UML tools are not flexible or adaptable, which makes understanding and code maintenance difficult, but some new tools may help with these challenges. Dynamic modeling tools will help users easily generate, modify, share, and save different types of UML diagrams. Automatically generated, interactive varieties of diagrams may soon become the norm, allowing users to understand their code faster and more intuitively.

As these tools become more intelligent and continue to stretch the boundaries of UML standards we can expect to see a rise in diagrams being used at all stages of development. But for now keep UML where it belongs, in the hands of experienced developers during the design process.

<div style="clear:both;">
  &nbsp;
</div>