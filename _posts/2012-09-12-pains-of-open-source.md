---
id: 372
title: Pains of Open Source
date: 2012-09-12T15:27:05+00:00
author: Vineet Sinha
layout: post
guid: http://blog.architexa.com/?p=372
permalink: /2012/09/pains-of-open-source/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Libraries &amp; Frameworks'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<img class="alignright size-medium wp-image-350" title="Open-Source" src="/assets/uploads/2012/05/Open-Source-1-300x269.jpg" alt="" width="210" height="188" srcset="/assets/uploads/2012/05/Open-Source-1-300x269.jpg 300w, /assets/uploads/2012/05/Open-Source-1.jpg 550w" sizes="(max-width: 210px) 100vw, 210px" />I am a big fan of open source. I use it every day, and recommend it often. But I do want to have a balanced perspective on it. I recently posted about the [pleasures of using open source](http://blog.architexa.com/2012/05/pleasures-of-open-source/). This is the other side of the coin, the pains of using it.

My hidden agenda about talking about such problems with open source usage is so that we as a community can come up with solutions to some of these challenges. But first, I really want to hear and write down the main challenges, so that we fix the right problems.<!--more-->

**Too many sub-par projects**

Perhaps it is that there is a lot of the not-invented-here syndrome that happens to us developers, or perhaps because most of the solutions to a particular problem are not good enough. But regardless, there are often way too many people putting effort into similar projects.

Now, I am not against having people try and build out different approaches &#8212; but there is a limit to that. For most frameworks that I have needed to try using as many as 3/4th of the projects are useless. Many projects were only developer to support a long deprecated api, and other projects are just not being maintained as the developers have found something more interesting (or perhaps something that might pay their bills).

Using the right framework often means trying out 2-3 solutions, going through its code to see how much it makes sense for your needs, and making sure that you are safe by being able to have your answer through determining the most active communities (in mailing lists, etc).

**Bag Of Bolts**

When 80% of the code in your project is an open source library, then most of your code is in figuring out how to hook up these projects together. Even though most libraries won&#8217;t force a way of using them, just integrating all their (open source) code bases is non-trivial.

By default, just bringing in such libraries will make your resulting web-app feel like a bag of bolts. Fortunately, project management and requirements usually take priority to such libraries, and therefore we as developers need to spend our time essentially becoming integration experts (to smooth out the kinks).

But here is the thing, the part that is unique to your application is in your code. So often, your 20% of the code is the hard part. While you might be using an open source search library like Lucene, it will be up to you to make sure that the indexes are not only created at the right time, with the right performance, but that they are stored in the right places, and have the right data in them. Some of these parts will be trivial as they are part of the default usage scenarios, but others might need the redesign of a key component of the library.

**The minor problems: Who to Pay, Licensing, and Versioning**

Using an open source libraries comes with an acknowledgement that we will get stuck, especially when we can&#8217;t figure out the code. Sites like StackOverflow are amazing, but some problems take more time to solve. I have often been in scenarios where we have a budget to give someone to solve the problem, but that we are often not sure as to who would be the best person/organization to give that to.

Sometimes, getting an open source library that gave us the freedom to do what we need is hard. Honestly, this used to be a big challenge, but recently most libraries are on a permissive license. Additionally, it can sometimes be a pain to update the versions of a library (tools like Maven and the entire ecosystem that Sonatype has fostered are incredibly helpful here).

**Summary/Thoughts**

I guess most of the above can be put simply put as &#8216;community&#8217; and &#8216;code readability/documentation&#8217;. With perhaps documentation helping to build community. I guess, coders love to code. And one of the first things that most developers do, is write code. The means that we should expect some Open Source libraries have very limited documentation. Most do have have decent documentation to help you get started, but are often limited when it comes to anything beyond that. Perhaps we need to incentivize the community of users (such as StackOverflow) to gain karma by helping to document some of these projects.

<div style="clear:both;">
  &nbsp;
</div>