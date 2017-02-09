---
id: 375
title: 'Diagramming Tools &#8211; A (Biased) Survey'
date: 2012-09-21T08:06:33+00:00
author: Christopher Deschenes
layout: post
guid: http://blog.architexa.com/?p=375
permalink: /2012/09/diagramming-tools-a-biased-survey/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Agile &amp; Development Methodologies'
  - 'Design Patterns &amp; Architecture'
  - Developer Tools
  - Java
  - 'UML &amp; Diagramming'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

Diagramming tools can help you to quickly understand a new project, debug code, visualize and enforce usage patterns, and quickly generate high quality documentation.  All good.  However, not all tools are created equal and there are lots of legacy tools (UML has been around for a while).  I wanted to take a look at what is out there to get a sense for how these tools are evolving.

Below is a slice if you will through what are some next generation offerings in software development, tools that are trying to do something different, and some well established old-guard tools that everyone has heard of and compares all comers too.<strong id="internal-source-marker_0.24177810037508607"></strong>

<img class=" wp-image-376 alignleft" title="Code Canvas Example" src="assets/uploads/2012/09/codecanvas-300x198.png" alt="Code Canvas Example" width="240" height="158" srcset="assets/uploads/2012/09/codecanvas-300x198.png 300w, assets/uploads/2012/09/codecanvas.png 777w" sizes="(max-width: 240px) 100vw, 240px" />

**Debugger Canvas  **[Debugger Canvas](http://msdn.microsoft.com/en-us/devlabs/debuggercanvas.aspx "Debugger Canvas") by Microsoft <strong id="internal-source-marker_0.25623594783246517">(see <a href="http://www.youtube.com/watch?v=tsFfyli2Y9s">video</a>)</strong> is based on Code Canvas which was developed at Microsoft Research in  collaboration with the Code Bubbles folks from Brown.  Debugger Canvas is available to premium Microsoft Visual Studio license holders.  I love how you can view a GUI widget, its documentation, and implementation side by side in one clean view.  The development metaphor is very different from a traditional IDE.
  

&nbsp;

<!--more-->


  
pfff** <img class="alignright  wp-image-377" title="Linux kernel in PFFF view" src="assets/uploads/2012/09/pfff_linux_0.01_c2-300x182.jpg" alt="Linux kernel in PFFF view" width="240" height="146" srcset="assets/uploads/2012/09/pfff_linux_0.01_c2-300x182.jpg 300w, assets/uploads/2012/09/pfff_linux_0.01_c2-1024x623.jpg 1024w, assets/uploads/2012/09/pfff_linux_0.01_c2.jpg 1350w" sizes="(max-width: 240px) 100vw, 240px" />pfff is an open source tool built by Facebook.  It works on their primary language PHP.  Here is a [link to pfff on GitHub](https://github.com/facebook/pfff).  In the author’s words “pfff is mainly an OCaml API to write static analysis, dynamic analysis, code visualizations, code navigations, or style-preserving source-to-source transformations such as refactorings on source code.”

It generates some interesting graphics that certainly help to conceptualize the software architecture of a code base.  Here is a [link to a code graph of linux](https://github.com/facebook/pfff/wiki/images/pfff_linux_0.01_c2.jpg).

&nbsp;

**LightTable** <img class="alignleft size-medium wp-image-378" title="game-example" src="assets/uploads/2012/09/game-example-300x187.png" alt="" width="300" height="187" srcset="assets/uploads/2012/09/game-example-300x187.png 300w, assets/uploads/2012/09/game-example-1024x640.png 1024w, assets/uploads/2012/09/game-example.png 1440w" sizes="(max-width: 300px) 100vw, 300px" />I’m also throwing something very interesting into the mix; [LightTable from Chris Granger.](http://www.chris-granger.com/2012/04/12/light-table---a-new-ide-concept/)   It is different.  LightTable provides an awesome metaphor for writing Clojure.  Python and other languages are supported.  “light” mode provides a spatial representation of code relationships and layout.

Pretty amazing!  This is a rather cool new IDE concept.  I love the way you can see your code running in your workspace while you edit it.  The image shows a game running.

&nbsp;

&nbsp;

**Google  **Google surprisingly has nothing that I can find although there a lot of tools listed if you search under [code.google.com](http://code.google.com/) for diagramming tools and java reverse engineering.  Does someone know any diagramming tools that are developed by/used by the Google folks?<strong id="internal-source-marker_0.24177810037508607"></strong>

**Gliffy and UMLet  **There are a number of tools out there, some web-based, some desktop-based, that provide the user with the ability to draw UML diagrams.  Gliffy and UMLet are great in that they don&#8217;t try to do code generation from diagrams &#8211; something that often does not work. This way they have focused on building an easy to use (albeit limited) tool.  These tools do not do reverse engineering.  Gliffy and UMLet are very popular choices but they are not “code-aware” as I understand it.  Their efficacy for understanding a code base and debugging are limited.<strong id="internal-source-marker_0.24177810037508607"></strong>

**Rational  **Ah yes.  The mighty Rational.  A powerhouse for a long time.  Perhaps too long.  Very strong on upfront design using MDA and heavy software lifecycle processes.  IMHO it is being disrupted significantly by agile  and lean development methodologies.  It is expense to acquire and the learning curve is not insignificant.  The next generation of tools is not encumbered by having to meet the raft of requirements that have amassed around Rational over the years.<strong id="internal-source-marker_0.24177810037508607"></strong>

**AgileJ/MaintainJ/ModelGoon  **Why these tools?  They certainly deserve mention and perhaps a closer look.  In some situations you want a commercially backed tool (so you have someone to yell at if something goes wrong).  Aligning with Agile processes certainly makes sense especially if the tooling really enables and compliments that style of development.

**Native IDE Capabilities &#8211; Yes &#8211; IntelliJ  **IntelliJ is a great IDE (Netbeans too!) and has pretty good support for integrated diagrams.  Together with the rest of what makes IntelliJ strong makes for a really powerful combination &#8211; code-aware diagrams that don’t suck.  One gap however is support for sequence diagrams.<strong id="internal-source-marker_0.24177810037508607"></strong>

**UML-Lab from Yatta  **The German offering is quite impressive.  Round-trip engineering between diagrams and code is a strong claim to make (because it is really hard to go each way with a high degree of reliability.)  Reverse engineering is pretty nifty too.  And it is for Java as well. UML-Lab doesn&#8217;t provide a high level overview of your code however.

**Architexa  **That&#8217;s us.  That&#8217;s where the &#8220;biased&#8221; comes from.  I&#8217;m not going to review our tools here or compare them to the tools listed.  Our philosophy though is that we love developers and want to make their lives better by helping them produce higher quality code and minimizing time spent on marginally valuable tasks.

**Didn’t Include Your Favorite?  **Yes I know.  I’ve neglected to mention [Enterprise Architect](http://www.sparxsystems.com.au/ "Enterprise Architect").  Let me know if there are other cool tools that should be mentioned here.  I simply don’t have time to do an exhaustive comparison.  No slight intended for tools not mentioned.

There are a lot of tools out there that target specific languages and versions of UML.  [Diagramming.org](http://www.diagramming.org "Diagramming.org") has a fairly extensive list of both proprietary and non-proprietary/open source diagramming tools.

**Common Theme  **One popular use for diagramming tools is helping developers when they are trying to understand a new code base.  Developers need ready access to the “architecture” though it may not be explicitly documented and not apparent from visual inspection of the code itself.  Yeah, my code is “self-documenting” because I’m so good, but your’s most likely is not.

By “new” project I mean that it was inherited or the developer is new to the team.  It could even be a new project.  Experience as a developer certainly helps but for a complex code base that has had developer churn you just can’t figure it out by trolling through the code &#8211; at least not as efficiently as you could with the right tools.

**The Bottom Line  **The tools included here are chosen to be more or less representative but to also include some innovative approaches.  The bottom line is that being able to automatically or at least semi-automatically (guided) generate visual depictions of complex code design and interactions can greatly reduce time wasted manually generating diagrams (which are out of sync with the code almost immediately.)

Most of these tools have either free trial downloads or are free for open source or individual use.  If you haven’t done so lately explore your code base with one of these tools.  Try using some of the diagrams in code reviews and architecture enforcement.  Let us know if you got bang for the buck for the time spent.

<div>
</div>

<div style="clear:both;">
  &nbsp;
</div>