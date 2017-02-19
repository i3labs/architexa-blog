---
id: 60
title: Types of Dependency Injection
date: 2010-05-04T07:02:08+00:00
author: Abhishek Rakshit
layout: post
guid: http://blog.architexa.com/?p=60
permalink: /2010/05/types-of-dependency-injection/
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

<div id="_mcePaste">
  <img class="alignright size-full wp-image-61" title="dep_Inj_types" src="{{site.baseurl}}/assets/uploads/2010/05/dep_Inj_types.jpg" alt="" width="280" height="300" />In continuation with my effort of trying to simplify <a href="http://blog.architexa.com/category/design-patterns-architecture/">Dependency Injection</a>, I want to elaborate on the different types of injection. Dependency Injection is decoupling an application and service so that the application does not need to know anything about the service implementation. Dependency injection can be broadly classified in three categories: Constructor, Setter and Interface.
</div>



<div>
  Object dependencies when passed as parameters to a constructor is termed as <em><strong>Constructor Injection</strong></em>.<br /> <code>&lt;br />
public class Account {&lt;br />
&nbsp;&nbsp;public User user;&lt;br />
&nbsp;&nbsp;public Account (User user) {&lt;br />
&nbsp;&nbsp;&nbsp;this.user = user;&lt;br />
&nbsp;&nbsp;}&lt;br />
}&lt;br />
</code></p> 
  
  <p>
    <a title="Pico Container" href="http://www.picocontainer.org/index.html" target="_blank">Pico Container</a> is a framework which prefers constructor injection. Constructor injection ensures that the application object is created with all its service dependencies satisfied. <!--more-->The constructor arguments clearly delineates the dependencies and makes the code easy to understand. Using constructor injection also relieves the developer to explicitly check for the validity of the created object i.e the constructor enforces that all the dependencies for the required object have been injected already. Another advantage of constructor injection is that immutable properties can be hidden by not providing a setter. If setters are used to initialize these objects it can become a problem because not having a setter clearly signifies that the object is non modifiable. The code snippet shown above is a simple example of an Account class where the dependency of User class is injected through the constructor.</div> 
    
    <div id="_mcePaste">
      But, there are cases where Constructor injection can get messy, like having a class with a lot of dependencies. A constructor with many parameters can make the code hard to manage. Moreover, when dealing with multiple constructors and inheritance one has to initialize the super class correctly while adding your own parameters too. In such cases, using <em><strong>Setter Injection</strong></em> might be a better choice. In Setter Injection an explicit setter method is responsible for injecting the desired dependency as shown below.
    </div>
    
    <div>
      <p>
        <code>&lt;br />
public class Account {&lt;br />
&nbsp;&nbsp;public User user;&lt;br />
&nbsp;&nbsp;public setUser (User user) {&lt;br />
&nbsp;&nbsp;&nbsp;this.user = user;&lt;br />
&nbsp;&nbsp;}&lt;br />
}&lt;br />
</code>
      </p>
      
      <div>
        The configurations to accomplish the injections can be set using XML or directly through code. One particular advantage of Setter injection is that it allows the creation of the resource as late as possible and only when it is needed. This is really useful in cases where the injected instance is expensive to create and is used rarely. The <a title="Spring" href="http://www.springsource.org/" target="_blank">Spring</a> framework prefers this type of injection although it does support constructor and interface injection.
      </div>
      
      <div>
        <br /> The third category is of <em><strong>Interface Injection</strong></em> where an interface defines the injection method. The method providing the implementation has to implement the interface and as such the service is dependent on the interface and not on the implementation.  The example below shows the Account class which depends on the IUser interface and the AccountController class injects the required dependency in this case the object of the User class which implements the IUser interface.</p> 
        
        <p>
          <code>&lt;br />
public class Account {&lt;br />
&nbsp;&nbsp;public IUser user;&lt;br />
&nbsp;&nbsp;public setUser (IUser user) {&lt;br />
&nbsp;&nbsp;&nbsp;this.user = user;&lt;br />
&nbsp;&nbsp;}&lt;br />
}&lt;/p>
&lt;p>public class AccountController {&lt;br />
&nbsp;&nbsp;public void initDefaultAccount () {&lt;br />
&nbsp;&nbsp;&nbsp;Account defaultUser = new Account;&lt;br />
&nbsp;&nbsp;&nbsp;defaultUser.setUser(new User());&lt;br />
&nbsp;&nbsp;}&lt;br />
}&lt;/p>
&lt;p>public class User implements IUser {&lt;br />
&nbsp;&nbsp;public String name;&lt;br />
&nbsp;&nbsp;public Long id;&lt;br />
...&lt;br />
}</code>
        </p>
        
        <p>
          <strong>Summary</strong>
        </p>
        
        <div>
          To sum up, Dependency Injection in itself a very good practice to keep your code understandable, efficient and robust. However, what type of injection to use depends more or less on your code. The constructor and setter injections are the more commonly used approaches and there is a lot of debate going on about which is better. Both of them have their strengths and weaknesses and a good rule of thumb which works for most cases is using constructor injection for required dependencies and setter injection for optional dependencies. More detailed information about Dependency Injection can be found <a href = "http://www.martinfowler.com/articles/injection.html" target="_blank">here</a>.
        </div>
      </div>
    </div>
    
    <div style="clear:both;">
      &nbsp;
    </div>