---
id: 168
title: 'REST Architecture &#8211; Simplified'
date: 2010-11-14T16:23:17+00:00
author: Abhishek Rakshit
layout: post
guid: http://blog.architexa.com/?p=168
permalink: /2010/11/rest-architecture-simplified/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Agile &amp; Development Methodologies'
  - 'Design Patterns &amp; Architecture'
  - Java
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<img class="alignright size-medium wp-image-172" title="rest_up" src="/assets/uploads/2010/11/rest_up-300x161.png" alt="" width="300" height="161" srcset="/assets/uploads/2010/11/rest_up-300x161.png 300w, /assets/uploads/2010/11/rest_up.png 430w" sizes="(max-width: 300px) 100vw, 300px" />Recently, while working on some collaboration functionality for our suite I got a chance to work on a <a href="http://en.wikipedia.org/wiki/Representational_State_Transfer" target="_blank">REST</a> (Representational State Transfer) based web server. There are many great resources about REST out there but most of them are quite technical and it took a me a while to get it. So, in this post I am trying to explain in some simple terms what I have understood about REST.<!--more-->

There has been a lot of interest about REST lately. Most of it is because of its features like being simple to implement and maintain REST also allowing projects to be scalable by supporting multiple back end services. Not only those, features like caching support and no contract architecture make REST an easy and quick way to setup an efficient web service. REST has often been <a href="http://www.taranfx.com/rest-vs-soap-using-http-choosing-the-right-webservice-protocol" target="_blank">compared</a> to SOAP  and even said to be better in some cases. In my view SOAP and REST both are great ways to interface with web services and both have their advantages and disadvantages and it is up to the developer to <a href="http://www.infoq.com/articles/rest-soap-when-to-use-each" target="_blank">understand</a> the need of his project.

REST is an architectural style to easily create, modify and delete resources. By definition, REST is a guideline to build an efficient framework for communication between two machines. In fact, the most common example of REST is the world wide web. There are a few major concepts which make REST unique from other web services such as unique url mapping, stateless architecture, limited action verbs and standard data exchange formats.

**Unique URL-Resource Mapping**

The basic fundamental of REST is that each and every resource is mapped to a unique URL, where a resource could be a web-page, file, image, video etc. The urls for each resource are not some randomly given path but should be based on some logical way to access information. The figure below is a simple example of a maps website with url’s forming a logical information access tree. Having these logical names makes it easy to cache query results improving overall performance.

<p style="text-align: center;">
  <a href="/assets/uploads/2010/11/restUrl.png"><img class="size-medium wp-image-169 aligncenter" title="restUrl" src="/assets/uploads/2010/11/restUrl-300x119.png" alt="" width="300" height="119" srcset="/assets/uploads/2010/11/restUrl-300x119.png 300w, /assets/uploads/2010/11/restUrl.png 627w" sizes="(max-width: 300px) 100vw, 300px" /></a>
</p>

**Statelessness**

REST is a stateless architecture, i.e. all the information required to process the request by the server is contained along with the request. This includes the url, headers, query parameters etc as no information of the previous request is maintained by the server. Being stateless may decrease network performance by repetition of data but thats the trade off for allowing us to balance the load across multiple servers which, if done correctly can negate any network performance issues. So for services where no operations needs to be continued REST can work really well.

**Action Verbs**

REST advises use of the four verbs GET, POST, PUT and DELETE for all its communication and resource handling. Many developers are suspicious of having only four verbs but I&#8217;ve found that for most applications these are more than enough. GET is used by the client to access the resources on the server. It is an idempotent request and as such makes no changes to the resource on the server. Once the client has the resource it can use POST/PUT to modify it or create a new resource. Keep in mind when choosing between these that PUT is idempotent and POST is not. So if you call the server multiple times with the same PUT request you will still have the same effect. But in case of POST the resource can be partially modified with separate requests. The following <a href="http://stackoverflow.com/questions/630453/put-vs-post-in-rest" target="_blank">discussion</a> can provide you more information about POST and PUT. DELETE as you might have figured is used to delete a resource but is not supported by most modern browser and hence is not used much.

**Data Exchange Formats**

Now that we know how the client and server interact the next key aspect is the format of the resource as it moves between them. XML and JSON (JavaScript Object Notation) are common structural forms to accomplish this. In our server we used JSON for its inherent javascript support allowing most browsers to process it easily. Apart from that, the XML format is verbose and takes time to parse and also creates an impedance mismatch when converting to and from a POJO.

**Summary**

Some concerns about the REST infrastructure lie in fact that it uses http authentication, which still has a lot of room for improvements. Regardless, being a lightweight, quick approach towards setting up a web service does make REST a great architecture to go with.

<div>
  Another interesting post by Ryan Tomayko about <a href="http://tomayko.com/writings/rest-to-my-wife" target="_blank">How I Explained REST to My Wife</a> does a great job in explaining REST in very simple terms.
</div>

Have you used REST? Please share your thoughts about it.

<div>
  <a href="http://www.flickr.com/photos/joeshlabotnik/419914250/sizes/z/in/photostream/" target="_blank">Image Credit: Joe Shlabotnik</a>
</div>

<div style="clear:both;">
  &nbsp;
</div>