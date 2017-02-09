---
id: 99
title: Is your code poorly commented? Three indicators..
date: 2010-07-08T20:45:49+00:00
author: Vineet Sinha
layout: post
guid: http://blog.architexa.com/?p=99
permalink: /2010/07/is-your-code-poorly-commented/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Documentation &amp; Communication'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-full wp-image-102" title="comic-book-guy-comment-sc" src="/assets/uploads/2010/07/comic-book-guy-comment-sc1.jpg" alt="" width="298" height="286" />](/assets/uploads/2010/07/comic-book-guy-comment-sc1.jpg)One fact that is agreed upon &#8211; is that it takes a lot of time to [understand code](http://blog.architexa.com/2010/05/no-you-are-not-dumb-programmers-do-spend-a-lot-of-time-understanding-code/). Poorly commented code just makes this harder. The challenge that we face, is that developers&#8217; often don&#8217;t want to take time away from coding to document, but working with code that is not commented takes more time in the long run.

It is always nice to work on a project that has excellent commenting. However, there have been many projects that I have worked on that have frustrated me with the effort needed in understanding them. When code that I have been writing needs to build on badly documented components, I have sometimes added my own comments. Tragically, I have often not been responsible for maintaining such components and my effort in commenting has gone to waste &#8211; as I have not checked them in. Such code often has had three traits.

<!--more-->

**1. When documentation in needed to understand _what_ is going on.**
  
Code sometimes is so cryptic that many lines of comments are needed to make sense of what is happening. If written well, this code would use clear variables and method names so that the logic is immediately obvious. Doing this not only helps in understanding what the code is doing, but also allows for comments to be used for describing why the code is needed (see item 3).

> <pre>/**
* calculate the amount of interest gained from a principal of p at a 
* rate of r over y years loop through each year and calculate the 
* new amount based on the rate. set the principal to the new 
* amount for interest compounded annually.
*/
public static float main(float p, float r, int y) {
  DecimalFormat format = new DecimalFormat( "0.00" );
  float a;
  for(int i=1;i&lt;=y;i++){a=p*(1.0+r);}
  p=a;
  return format.format( a );
}
</pre>
> 
> The lack of useful variable names and structure in this code prevents it from being easily read, necessitating the use of comments to describe what it does

**2. When there is more comment header than actual useful comments.**
  
In the quest for helping developers writing comments quickly, development tools often generate comment headers when creating new classes, methods, etc. While such headers can be helpful, leaving them as-is makes it harder for us to detect the signal (the actual useful comments) from the noise (the automatically generated headers). Instead filling in these headers can make understanding easier.

> <pre>/**
* @param principal
* @param rate
* @param years
* @return compundedInterest
*/
public static float calcInterest(float principal, float rate, int years) {
  DecimalFormat precisionTwo = new DecimalFormat( "0.00" );
  float amount;
  for ( int year = 1; year &lt;= years; year++ )
  {
    amount = principal * (1.0+rate);
    principal = amount;
  }
  return precisionTwo.format( amount );
}
</pre>
> 
> Here we see how automatically generated headers become useless noise when left as is.

**3. When it is not obvious **why** a piece of code behaves in a particular way.**
  
One can always figure out what a piece of code is doing (although sometimes it can take a lot of effort). The challenge however, is that if not documented, it is impossible to figure out why the code needs to behave in the way that it does. When writing code, it is therefore important to ask yourself the &#8216;whys&#8217; and to make sure that it is included in code comments.

> <pre>/**
* Calculate compound interest for accounting form 2-a.
* We are calculating the interest by using a loop instead of
* principal*(1+rate)^years to show the exact workings of the compounded
* interest calculation
*/
public static float calcInterest(float principal, float rate, int years) {
  DecimalFormat precisionTwo = new DecimalFormat( "0.00" );
  float amount;
  for ( int year = 1; year &lt;= years; year++ )
  {
    amount = principal * (1.0+rate);
    principal = amount;
  }
  return precisionTwo.format( amount );
}
</pre>
> 
> An example of a quality comment describing why the code is needed and why it was written the way it was

**Other resources**
  
For other tips on improving comments and code quality see the following articles:

  * [Four Things to Know when Writing Comments](http://java.dzone.com/news/four-things-know-when-writing) at JavaLobby
  * [Six ways to write more comprehensible code (How to keep your code from destroying you)](http://www.ibm.com/developerworks/linux/library/l-clear-code/) at IBM developerWorks
  * [Writing Good Code](http://www.bioinformaticszen.com/software/writing_good_code/) at Bioinformatics Zen

<div style="clear:both;">
  &nbsp;
</div>