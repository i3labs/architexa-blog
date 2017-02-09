---
id: 9
title: Eliminating the Suck in Your Software
date: 2010-02-26T17:00:38+00:00
author: Elizabeth Murnane
layout: post
guid: http://blog.architexa.com/?p=9
permalink: /2010/02/eliminating-the-suck-in-your-software/
categories:
  - User Experience
tags:
  - usability
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<div class="picture">
  <img src="assets/uploads/2010/03/SoftwareSucks.jpg" alt="Software Sucks!" width="282" height="216" />
</div>

Recently Microsoft NERD hosted a talk by David Platt, and according to David, users think that today&#8217;s software sucks. He says it is overcomplicated, too hard to use, and simply doesn&#8217;t get its job done. It is true that software is a top consumer complaint. David cites statistics from the Better Business Bureau regarding most complaints received per industry, and software industries appeared three times in the top 7 in 2006 and three times in the top 5 in 2007.

But before you slit your throat, I say consider when viewing these statistics how ubiquitous technology and software services are today. Even if a much smaller industry sucked a lot more, software industries would still rank higher in a list of the number of received complaints simply because the number of consumers in the small industry is far less than the number of software users. Really what I&#8217;d like to know is the number of complaints our industry receives compared to the number of possible complainers (our users). Of course, regardless of whether these statistics are the best gauge of user satisfaction, it would be foolish to not make an effort to determine what the complaints against your software are or to ignore major design flaws.

<!--more-->

David tells us that a likely cause for the large number of unhappy software consumers is the dramatic change in the number and background of users today. There has been a huge growth in the size of the user population and a corresponding decrease in their comparative skills. This change in the quantity, composition, and quality of users means that they no longer resemble developers. Developers and users used to be the same people. In 1994 there were 2 million web users who were predominantly research scientists or people with a technical background. By 2008 there were 14 million web users, and they had a profile similar to the general population. While developers are almost entirely male, 52% of users are female. Almost all developers go to college, but 82% of users have no college degree. Developers highly value control, as evidenced by the large percentage that drives manual cars; only 12% of users drive a manual car.

The take home message, which David repeats multiple times, is &#8220;Your users are not you.&#8221; Today&#8217;s users simply want their software to accomplish the task at hand, and they prefer a product that gets them to that result as quickly and easily as possible. They want software that &#8220;just works&#8221; as expected, and they don&#8217;t care how.

We at Architexa are in a somewhat unique position because _our users actually are developers_. It still holds true, however, that our users are not us. They do not care about our product the way that we do; they just want a tool that can help them work better with lots of code. We remind ourselves that we still need to keep the user in mind when viewing our product. We need to realize that the user&#8217;s perspective is not the same as ours, and we still must apply to ourselves the following guidelines for good software design. <!--more-->

**Good software accepts how a user behaves** and doesn&#8217;t require him to work against his instincts to get the desired result. Good software also adapts to human imperfection rather than forcing users to be robotically meticulous. Consider two features of Microsoft Word. Word&#8217;s drag-able file toolbar probably seemed like a super cool feature to the developer who implemented it, but to a user it is a major annoyance that forces him to be more precise than necessary and punishes him when he is not. Alternatively, the automatic spelling fix feature understands the user&#8217;s humanity, anticipates user frailty, and compensates for it.

**Good software also treats the user well** and is helpful and considerate. Take the main pages of Google and UPS as examples. Google automatically chooses the language that the user would most likely want based on their location and makes it easy to change if wrong. On the other hand, UPS&#8217;s start page requires that a user enter a location before access to the website is granted. This requirement is not user friendly and sends a negative &#8220;We are in charge&#8221; message, as David puts it, to the user.

Basically, good software tries to take care of the user, and **it doesn&#8217;t have extra features or pages that make life harder for the user**. Developers love creating elaborate features and offering multiple customization options, but developers need to remember to always ask: Does X enhance our product or can we get our message across without it? Consider the iPhone. It was more successful than other phones on the market because even though it was more expensive and had less functionality, its user experience didn&#8217;t suck. Apple&#8217;s main focus was not implementing a particular feature, app, or capability but rather figuring out what people used a phone to do and creating an interface that actually worked well to do those things. Similarly at Architexa, we must remember that the most important thing to our users is that they understand their code. They would only want and use the additional control if it helped them achieve this comprehension goal more effectively.

David also stresses that developers need to be sure not to underestimate the effect of &#8220;constant friction&#8221;. To a user, clicks = time = money. Even if it is only one extra mouse click every few hours or a few extra seconds wasted per task, when multiplied by all the users over a period of time, the result can be a lot of the client&#8217;s time and money wasted, and that will not make the client happy. David lastly made the following good recommendations for creating better software:

1. **Add to your team** someone who is a non-technical person and/or doesn&#8217;t know the internal workings of your program. You want the people who test your software to represent your user demographic.

2. **Break with convention if necessary**. Even if most programs don&#8217;t do something, if doing it is what&#8217;s best for _your_ program, do it. Also, over time users have changed, and therefore old conventions may no longer apply.

3. **Don&#8217;t let edge cases complicate the mainstream**. Developers are conditioned to think in terms of perfection; if a math theorem only works in 99 out of 100 cases it&#8217;s no good, but if an application doesn&#8217;t work for 1 person out of 100, the focus should stay on keeping the other 99 happy. Generality is good, and assumptions are fine if they work for most cases.

4. **Instrument carefully** while ensuring that the application isn&#8217;t intrusive and doesn&#8217;t gather sensitive data. Be wary of using focus groups and try monitoring real, actual users to learn what interfaces they like and what needs to be made simpler. For your website, figure out what visitors think about it by determining what pages they view and in what order. For desktop apps, David recommends using his free program available at [knowthyuser.com](http://www.knowthyuser.com) in order to instrument the user interface and see what users are actually doing.

Related to #4, I think that it is additionally very important for developers to provide users with a good method for providing feedback &#8211; but I also think that this is one of the hardest things to do well. Users are hesitant to talk about their difficulties for fear of appearing stupid, and some users avoid mentioning gripes in order to be polite, making it hard to know how reliable their feedback is. Also, if you ask a question about a specific feature, a user is much more likely to try to critique that feature or give suggestions on how to improve it than to say it should be eliminated entirely, even if that is what they would prefer. Finally, examining feedback and results of instrumentation can be time consuming and expensive for the software team, so a representative sample may not end up being examined.

5. Finally, **always ask**: Is this individual design decision taking our program closer or farther from &#8220;just working&#8221;? The goal should always be to increase the usability of the software rather than to advance an imagined idea that seems impressive or interesting to the developer but that doesn&#8217;t necessarily help the user. Remember that the user has different expectations and needs because the user is not you!
  
  
</br>

<small>(Image via <a href="http://www.flickr.com/photos/40108736@N08/4271821725/">Flickr</a>)</small>

<div style="clear:both;">
  &nbsp;
</div>