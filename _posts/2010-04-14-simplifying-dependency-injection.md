---
id: 26
title: Simplifying Dependency Injection
date: 2010-04-14T17:21:58+00:00
author: Abhishek Rakshit
layout: post
guid: http://blog.architexa.com/?p=26
permalink: /2010/04/simplifying-dependency-injection/
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

[<img class="size-medium wp-image-27 alignright" title="Dependency Injection" src="assets/uploads/2010/04/vilcus-plug-it-in-208x300.jpg" alt="" width="187" height="270" srcset="assets/uploads/2010/04/vilcus-plug-it-in-208x300.jpg 208w, assets/uploads/2010/04/vilcus-plug-it-in.jpg 533w" sizes="(max-width: 187px) 100vw, 187px" />](assets/uploads/2010/04/vilcus-plug-it-in.jpg)
  
A lot has been written about _Dependency Injection_ (DI) however, it still remains a complicated topic. The [main](http://martinfowler.com/articles/injection.html) articles on this [topic](http://en.wikipedia.org/wiki/Dependency_injection) are quite thorough and provide really good information but in the process, the basic principle behind DI becomes hard to comprehend. DI is in fact fairly simple &#8211; its main goal is removal of a class dependency on some code. This class dependency is then &#8216;injected&#8217; into the code where it is needed. Using dependency injection helps in code maintenance, re-usability, testability, and improves code readability.

**An Explanatory Example**
  
In one of my projects, we needed to use DI to inject different implementations into a core service. Our project needed to be deployed to multiple types of servers while we wanted to share large portions of the core code and at the same time have different functionality for users.

<!--more-->


  
At its simplest, all we needed to do for DI was:

`<br />
public class Account {<br />
&nbsp;&nbsp;public User user = new DefaultUser();<br />
&nbsp;&nbsp;public UserPrivileges getUserPrivileges() {<br />
&nbsp;&nbsp;&nbsp;&nbsp;return user.getPrivileges();<br />
&nbsp;&nbsp;}<br />
}<br />
` 

Among other tasks, the Account class is responsible for getting users information, which it does by depending on the User class (or interface) to provide the functionality. We can have multiple classes extending the User class to provide different implementations of the getPrivileges method.

`<br />
public class Controller {<br />
&nbsp;&nbsp;public void getAdminUserAccount(){<br />
&nbsp;&nbsp;Account account = new Account();<br />
&nbsp;&nbsp;// Controller injects the admin user, overriding the default user<br />
&nbsp;&nbsp;account.user = new AdminUser();<br />
&nbsp;&nbsp;return account;<br />
&nbsp;&nbsp;}<br />
}<br />
` 
  
The Account class needs to only depend on the User class and customized implementations can be injected by setting the user field as shown in the second code snippet.

Since the dependency in the Account class is injected externally, hence the name Dependency Injection. To put it technically, the User class is the &#8220;dependant&#8221;, the overrides are the dependencies and the method which sets the override field is the &#8220;injector&#8221;.

**Benefits**
  
DI helps to re-use code in different contexts with customized implementations. It can also be used when code needs to be given to third-party users who can then plug in suitable implementations. Apart from the mentioned benefits, DI can be used to break code cycles and also for code testing since it allows the dependencies to be mocked or stubbed out. DI removes unnecessary dependencies and makes the code more portable as the dependencies are mostly on interfaces. It also helps in eliminating dependency carrying. Dependency carrying is the concept of a method passing on object(s) which it does not use itself. So, all that the method does is pass on the object(s) to some other method. Instead the object(s) can be injected directly to the method which uses them and not through a chain of methods which only act as carriers. All in all, DI can make your code easy to manage and change.

**Complications with DI**
  
As always there are some complications with DI such as added indirection in the code, as the injection is performed externally. In cases where the implementation is not always accessible understanding code can become hard. Moreover, when using a framework to DI, the controllers themselves are hard to test and managing the configuration files (for frameworks maintaining verbose configuration files) is a cumbersome task when the project becomes large.

**Any Thoughts?**
  
What do you find complicated in DI? In which scenario was DI helpful to you or Are there cases where you avoided using it? Share your thoughts about Dependency Injection.

<span style="font-size: 0.8em;"><em><br /> </em> </span>

<div style="clear:both;">
  &nbsp;
</div>