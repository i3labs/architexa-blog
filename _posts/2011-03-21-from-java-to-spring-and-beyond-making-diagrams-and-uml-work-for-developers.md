---
id: 241
title: 'From Java to Spring and Beyond &#8211; Making Diagrams (and UML) work for developers'
date: 2011-03-21T17:49:35+00:00
author: seth
excerpt: |
  One of the strengths of working with Java is the large number of frameworks that are available. These frameworks are great for taking care of the basic tasks involved in building Java based apps. But they often bring about challenges in understanding - whether it is xml files or annotation based configurations, developers needing to work with these frameworks have to see how different parts of the code are connected.
  
  With this in mind we have extended Architexa to not just show code relationships but have also built special support for popular frameworks like Spring and Struts. We are happy to announce that we will be demoing this functionality at EclipseCon 2011 as part of the Hot New Products Showcase.
  
  We are pushing the edge here - so we are making this capability available as an 'early access' version. You can find it by default in all versions of the Architexa Suite. We would really like to hear what you think about it, and invite you to extend your trial of the product as we refine the implementation based on your feedback
  
  In this release we are including early access to a number of frameworks. With Spring we have added support for Dependency Injection and Web Flow. We have also added support for Struts (1 and 2) and Tiles.
  
  Spring Bean classes can be shown in both class and sequence diagrams along with any Property fields they contain. This allows for easy exploration of the hierarchy of beans along with a clearer view of dependency injection.
  
  Struts support enables you to explore the actions defined in xml configurations files; specifically, the dependencies to other actions, jsp pages, and classes all within an easy to understand class diagram.
  
  Tiles support allows you to easily see where different JSPs plug into various web components and how they relate to other java elements in a class diagram.
layout: post
guid: http://blog.architexa.com/?p=241
permalink: /2011/03/from-java-to-spring-and-beyond-making-diagrams-and-uml-work-for-developers/
wpbb_sync_comments:
  - 'yes'
categories:
  - Developer Tools
  - Eclipse
  - Java
  - 'UML &amp; Diagramming'
tags:
  - eclipse
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<div>
  <div>
    <a href="/assets/uploads/2011/03/spring-struts.png"><img class="alignright" title="spring-struts" src="/assets/uploads/2011/03/spring-struts.png" alt="" width="251" height="175" /></a>One of the strengths of working with Java is the large number of frameworks that are available. These frameworks are great for taking care of the basic tasks involved in building Java based apps. But they often bring about challenges in understanding &#8211; whether it is xml files or annotation based configurations, developers needing to work with these frameworks have to see how different parts of the code are connected.
  </div>
  
  <div>
    With this in mind we have extended Architexa to not just show code relationships but have also built <a href="http://www.architexa.com/user-guide/JavaExtensions" target="_blank">special support</a> for popular frameworks like <a href="http://www.springsource.org/">Spring </a>and <a href="http://struts.apache.org/">Struts</a>. We are happy to announce that we will be demoing this functionality at <a href="http://www.eclipsecon.org" target="_blank">EclipseCon 2011</a> as part of the Hot New Products Showcase.
  </div>
  
  <div>
    We are pushing the edge here &#8211; so we are making this capability available as an &#8216;early access&#8217; version. You can find it by default in all versions of the<a href="http://www.architexa.com/start/index"> Architexa Suite</a>. We would really like to hear what you think about it, and invite you to extend your trial of the product as we refine the implementation based on your feedback
  </div>
  
  <div>
    <p>
      <!--more-->
    </p>
    
    <p>
      In this release we are including early access to a number of frameworks. With Spring we have added support for Dependency Injection and Web Flow. We have also added support for Struts (1 and 2) and Tiles.
    </p>
  </div>
  
  <div>
    <ul>
      <li>
        Spring <em>Bean</em> classes can be shown in both class and sequence diagrams along with any <em>Property </em>fields they contain. This allows for easy exploration of the hierarchy of beans along with a clearer view of dependency injection.
      </li>
      <li>
        Struts support enables you to explore the <em>actions</em> defined in xml configurations files; specifically, the dependencies to other actions, jsp pages, and classes all within an easy to understand class diagram.
      </li>
      <li>
        Tiles support allows you to easily see where different JSPs plug into various web components and how they relate to other java elements in a class diagram.
      </li>
    </ul>
  </div>
</div>

<div>
  For more information on our enterprise java support, see our reference page <a href="http://www.architexa.com/user-guide/JavaExtensions" target="_blank">here</a>.
</div>

<div>
  Also, be sure to take a look at our newly added support for <a href="http://wp.me/pOHlD-3Q">code review and architectural review</a>.
</div>

&nbsp;

<div style="clear:both;">
  &nbsp;
</div>