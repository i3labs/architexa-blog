---
id: 79
title: Cohesion and Coupling in Large Projects
date: 2010-06-01T20:48:55+00:00
author: Abhishek Rakshit
layout: post
guid: http://blog.architexa.com/?p=79
permalink: /2010/06/cohesion-and-coupling-in-large-projects/
categories:
  - 'Design Patterns &amp; Architecture'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<img class="alignright size-full wp-image-80" title="Cohesion and Coupling" src="/assets/uploads/2010/06/huddle.jpg" alt="" width="320" height="213" srcset="/assets/uploads/2010/06/huddle.jpg 500w, /assets/uploads/2010/06/huddle-300x199.jpg 300w" sizes="(max-width: 320px) 100vw, 320px" /><a href="http://en.wikipedia.org/wiki/Cohesion_(computer_science)" target="_blank">Cohesion</a> and [Coupling](http://en.wikipedia.org/wiki/Coupling_(computer_science)) are commonly used metrics to gauge the design quality of a software project with regards to maintainability, reuse and understandability. These issues are commonly faced by developers working with large codebases. The mantra for these issues is to have a _highly cohesive and loosely coupled code__base_.

Simply stating, **Cohesion means placing related code in one particular unit and Coupling is the degree of dependency between two or more units.** If the code is highly coupled i.e. different units depend a lot on each other and modifying one feature can cause unwanted side effects. To avoid these the developer has to understand each of the related classes to update the behavior safely. Loosely coupled code is easier to reuse and on modification does not have undesired ripple effects in the code base. Adding to the benefits highly cohesive code promotes easy code understandability as everything is placed closely together. These aspects are not restricted to classes but apply to everything from methods in a class to packages in a project.

<!--more-->An interesting term I read a while ago was a class being termed internally as a ‘coupled blob’. The methods and properties in a class should agree with each other on what common behavior they all fall under vaguely justifying the term. A good OO developer strives to make the class reasonably close knit when it comes to the functionalities that a class is supposed to provide. If the class starts getting bigger and complicated it’s on the way towards becoming an external coupling hub and its probably a good time to start refactoring.

Although, it is unrealistic to expect everything related to a particular behavior in one unit, following some simple rules can help. Steps like providing intuitive names to methods and classes, moving closely related functionalities to a common class, or moving unrelated stuff out into appropriate classes, goes a long way towards helping to maintain a healthy code-base. Moreover, coupling in a project cannot be completely eliminated but needs to be controlled and a good start is to focus on de-coupling high-level components like packages. Controlling coupling at the coarse-grained level tends to eliminate a major part of the day-to-day issues we face. The <a href="http://blog.architexa.com/2010/04/simplifying-dependency-injection/" target="_blank">Dependency Injection</a> design pattern is also a good way to control coupling as it promotes having dependencies to an interface instead of concrete objects.

As with every coding practice misapplication of cohesion and coupling can create problems instead of solving them. Sometimes pushing cohesion too far can result in diminished returns when the cohesion strength rises to a point where it actually starts to hurt quality not improve it. This is often due to addition unnecessary code complications. Moreover pushing excessively towards a loosely coupled architecture can become a deterrent to optimizations and increase overhead due to added abstraction layers. In the end it is the developer who has to find the right balance between making the code-base more maintainable and understandable without adding performance issues to the application.

Note: Let us how you managed to strike the right balance with regards to cohesion and coupling to make your project better.

<div style="clear:both;">
  &nbsp;
</div>