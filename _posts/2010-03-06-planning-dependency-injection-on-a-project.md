---
id: 65
title: Dependency Injection, Frameworks, and You
date: 2010-03-06T22:43:41+00:00
author: Abhishek Rakshit
layout: post
guid: http://blog.architexa.com/?p=65
permalink: /2010/03/planning-dependency-injection-on-a-project/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Design Patterns &amp; Architecture'
  - 'Libraries &amp; Frameworks'
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<img class="alignright" style="border: 0px initial initial;" src="http://farm3.static.flickr.com/2601/3914729343_6ba95723dc_m.jpg" border="0" alt="3D Character and Question Mark" width="180" height="240" />
  
I have previously [tried](http://blog.architexa.com/2010/05/types-of-dependency-injection/) explaining Dependency Injection and how it can be beneficial to any project. This leads us to an important question about whether to use a framework or to do injection manually. Using a framework all the time may not provide you with additional control, rather at times it may further complicate the code. On the other hand implementing dependency injection manually can sometimes become more time consuming and painful. So how do we actually choose?
  
<!--more-->


  
Both approaches have their pros and cons; manual DI is simple to implement and works well for small projects whereas using an external container/framework makes sense in a large project with many team members because it provides a consistent manner of doing things across the project.

There is no learning curve when doing manual DI and with the current IDE’s it is easy to find who calls the method to inject the implementation. Even developers who are not very familiar with DI can contribute to the project. Unlike the manual approach, when using a container there is a learning curve. However, once you understand the framework it helps you manage your projects with ease. The wiring, scopes and rules of instantiation are all declarative. This makes it easy to understand how the application is wired together and therefore easier to change. Moreover while testing, fake implementations are sometimes needed in place of key components and an automated framework does this for you. Also, there is no need to write factory classes by hand any more as the framework takes care of creating and returning the correct objects for you.

On the flip side, some frameworks which maintain verbose configuration files mandate that the developer understands code in addition to the configurations beforehand, which can become an added overhead.

[Spring](http://www.springsource.org/), [PicoContainer](http://www.picocontainer.org/index.html), [Guice](http://code.google.com/p/google-guice/), etc. are some frameworks which one can use for Dependency Injection. Below are some features to help you decide what you want.
  
_****_

_**Supported Injection Type**:_ I have mentioned in detail about dependency [i](http://blog.architexa.com/2010/05/types-of-dependency-injection/)njection [types](http://blog.architexa.com/2010/05/types-of-dependency-injection/) previously. All the containers currently support many types of injections (setter, constructor, interface, field etc). However, Spring prefers Setter Injection though Guice and Pico prefer Constructor Injection.

_**Annotations**:_ For some, use of annotations can be really compelling as it clearly delineates what dependency is being injected in the code and you do not have  to examine the configuration file. But for others it may seem to spatter the code with unnecessary information and couple it with the frameworks jars, which might seem to be exactly opposite of what is the point of Dependency Injection; creating a loosely coupled system.

_**Third party injection**:_ When it comes to injecting third party components into your project Spring provides you direct support for this. In Guice however, there is a roundabout approach for this as in most cases you cannot inject annotations into third party components. So a custom provider needs to be written to wire up the component.

_**Type Safety**:_ Guice and Pico are both Type Safe as everything is present in the code itself and is statically checked at compile time. Using JavaConfig in Spring is a type safe option although if you use external configuration files (XML), theoretically runtime errors can occur. Even then those errors are all caught early as the framework does check eagerly on loading.

_**Speed**:_ To some it may be important but conclusive comparisons among frameworks is not yet available. However according to some; Guice seems to be more lightweight and faster that both Pico and Spring. Spring is much more that just a dependency injection container and as such will have a large code footprint.

_**External Configuration files**:_ External configuration files seem to be a good way of keeping your code free from framework related stuff but if the project becomes really large with multiple configuration files it can become hard to understand what dependency configuration goes where. Spring supports external configuration through XML files but Guice and Pico does not.

_**Leverage existing IDE capabilities**:_ Most of the frameworks leverage current IDE capabilities to support the user like easy refactoring. Pico and Guice have more support here as everything is inside the code but when using external configuration files which may not be always visible to the IDE it may be a problem.

**TakeAways**

All these frameworks have been around for sometime and each framework has its own strengths. You should choose one  from the above criteria depending on your project needs. No matter which one you chose or even if you go on and make your own DI container, you will benefit immensely by keeping your code easily testable and manageable.

_Update(May 10, 2010):_ Updated _Supported Injection Type_ comment regarding Guice and Spring injection preference.

<a title="Attribution-NonCommercial License" href="http://creativecommons.org/licenses/by-nc/2.0/" target="_blank"><img src="http://blog.architexa.com/wp-content/plugins/photo-dropper/images/cc.png" border="0" alt="Creative Commons License" width="16" height="16" align="absmiddle" /></a> <a href="http://www.photodropper.com/photos/" target="_blank">photo</a> credit: <a title="姒儿喵喵" href="http://www.flickr.com/photos/40780016@N02/3914729343/" target="_blank">姒儿喵喵</a>

[val writing](http://valwritings.net/)|

<div style="clear:both;">
  &nbsp;
</div>