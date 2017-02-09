---
id: 310
title: 'Diagrams in Open Source &#038; Successful Development'
date: 2011-09-07T16:15:15+00:00
author: novita
layout: post
guid: http://blog.architexa.com/?p=310
permalink: /2011/09/diagrams-in-open-source-successful-development/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Documentation &amp; Communication'
  - Understanding Developers
tags:
  - eclipse
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-medium wp-image-311" title="opensource_logo" src="assets/uploads/2011/09/opensource_logo-300x258.gif" alt="" width="210" height="181" srcset="assets/uploads/2011/09/opensource_logo-300x258.gif 300w, assets/uploads/2011/09/opensource_logo.gif 400w" sizes="(max-width: 210px) 100vw, 210px" />](assets/uploads/2011/09/opensource_logo.gif)

When development teams are in the same room, it is not surprising to see diagrams being used &#8211; if only being shared via sketches made on pads, or through the use of whiteboards. Interestingly, despite the fact that OSS teams are distributed geographically, diagrams also play an important role in OSS development.

There was a helpful <a href="http://classes.engr.oregonstate.edu/eecs/winter2009/cs562/OSS-camera_ready.pdf" target="_blank">research</a> done by Koji Yatani et al. at University of Toronto and Oregon State University. They studied developers on the Ubuntu project and found that developers create and distribute digitalized diagrams as opposed to physical sketches. While the uses of diagrams are specific to the Ubuntu projects, there are definitely lessons that we can learn to apply in other OSS projects to ensure successful development.

<!--more-->

<span style="text-decoration: underline;"><strong>Role of Diagrams</strong></span>

Diagrams play a role in the Ubuntu project as part of design documentation. According to a Ubuntu developer, a diagram created in the design stage should remain as part of the project documentation. This form of design documentation is more for internal use among developers, and should not be confused with documentation for users or secondary stakeholders.

**Documentation for internal use:** Design diagrams in the form of ASCII arts are frequently used because they are light-weight, everybody can modify it and is without the compatibility issues that other diagramming formats have. ASCII arts are often helpful for showing how the internal structure of the code works. According to a developer in the Ubuntu team, using ASCII art for these purposes “actually works”.

**Communicating complex infrastructure and algorithms:** In Ubuntu development, just like any other OSS projects, communication relies primarily through the Internet. For instance, contributors often have ad-hoc meetings and informal discussions over e-mail or IRC. However, it is often difficult to express their designs clearly through such channels and contributors often argue about which is the better approach, the best tool or workflow.  Sometimes, there can also be concepts like multiple servers infrastructure that require long paragraphs to explain. In such cases, developers have produced diagrams for their proposed infrastructure or produced diagrams of already built design to communicate them clearly and more efficiently.

**Ensuring long-term survival of projects:** Like most OSS projects, the Ubuntu project is largely volunteer-based with a high turnover of contributors. Providing architectural diagrams of the existing system is one way to make the existing project understandable to potential contributors and lowers the barriers of entry for potential contributors. This is essential for ensuring the long-term survival of OSS projects. According to a Ubuntu developer surveyed in the study, this is in fact necessary because otherwise newcomers would be completely lost.

<span style="text-decoration: underline;"><strong>Challenges for Using Diagrams</strong></span>

It was found that OSS developers realize and understand the inconveniences of digitalized diagrams. For example, different people use different tools to generate the diagrams and it is troublesome to export and import diagrams of differing formats, creating incompatibility concerns. Another cause for concern is that sharing the diagrams is not easy. In particular, most OSS project mailing lists prohibit or frown upon attaching diagrams in postings. While OSS contributors often go around this problem by uploading them on external websites and attaching the links for the images in the postings, modifying and updating the diagrams become troublesome.

<span style="text-decoration: underline;"><strong>Final Thoughts&#8230;</strong></span>

Interestingly, despite such inconveniences, diagrams are often used in the Ubuntu project in the ways described above. This indicates that diagrams play an important role in the process of open source software development despite the lack of diagramming support.

What do you guys think? Is there any way that you use diagrams and would like to see tooling that has them being made easier for you? We have been feeling this pain that developers feel when working on such development projects. We are going to try to address them in the next few days. Let us know what you would like to see.

&nbsp;

&nbsp;

<div style="clear:both;">
  &nbsp;
</div>