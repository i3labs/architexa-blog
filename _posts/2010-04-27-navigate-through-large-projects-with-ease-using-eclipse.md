---
id: 43
title: Navigate through Large Projects with Ease using Eclipse
date: 2010-04-27T06:53:01+00:00
author: Abhishek Rakshit
layout: post
guid: http://blog.architexa.com/?p=43
permalink: /2010/04/navigate-through-large-projects-with-ease-using-eclipse/
categories:
  - Developer Tools
  - Java
tags:
  - eclipse
  - Navigation
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

<img class="alignright size-full wp-image-50" alt="" src="{{site.baseurl}}/assets/uploads/2010/04/compass1.jpg" width="159" height="240" srcset="{{site.baseurl}}/assets/uploads/2010/04/compass1.jpg 331w, {{site.baseurl}}/assets/uploads/2010/04/compass1-198x300.jpg 198w" sizes="(max-width: 159px) 100vw, 159px" />When working with large code bases, finding your way around can sometime get quite challenging. In such cases, Eclipse makes a developer&#8217;s life a lot easier with its shortcuts and quick navigation features. Below is a compilation of a few shortcuts that I have found really useful.

**_Quick Navigation in the Workspace_**

While working with a large projects one of the challenges we face is to quickly find resources in the workspace. A very useful resource is <a class="in-cell-link" style="font-family: Arial;" href="https://studentshare.net/statistics" target="_blank">https://studentshare.net/statistics</a> or shortcut to find any kind of Java resource is **Ctrl+Shift+T**. It opens a dialog box to search for the needed resource and wildcards can be used in cases where you are not sure about the name of the class. Similarly **Ctrl+Shift+R** can be used to find any type of resource (even non Java) present in the workspace like jsp’s, xml’s etc.

<!--more-->

<div id="attachment_47" style="width: 252px" class="wp-caption aligncenter">
  <a href="{{site.baseurl}}/assets/uploads/2010/04/openRes.png"><img class="size-full wp-image-47      " title="Find a resource (Ctrl+Shift+R)" alt="" src="{{site.baseurl}}/assets/uploads/2010/04/openRes.png" width="242" height="280" srcset="{{site.baseurl}}/assets/uploads/2010/04/openRes.png 328w, {{site.baseurl}}/assets/uploads/2010/04/openRes-258x300.png 258w" sizes="(max-width: 242px) 100vw, 242px" /></a>
  
  <p class="wp-caption-text">
    Find a resource (Ctrl+Shift+R)
  </p>
</div>

<p style="text-align: left;">
  During refactoring or debugging we need to know what all methods call a given method. In such cases <strong>Ctrl+Alt+H </strong>comes in really handy and shows all the callers of this method. It lists all other methods that would be affected when changing the selected method. Also in the call-hierarchy view one can see all the called methods from this method. (Just remember to switch back to default otherwise you might get confused the next time you use it.)
</p>

If you want to quickly see the class hierarchy to understand the inheritance structure, or find methods which one can override, or which have been overriden in sub classes, use **Ctrl+T.** 

If you like to have multiple files open in the editor, **Ctrl+E** list all of those for you. Moreover, having so many files open can make you lose track about the location where you made the last change. Just press **Ctrl+Q** to get to the last edited location.

**_Quick Navigation within a file_**

When dealing with large files use **Ctrl+L** to jump to a particular line in the file. Although an outline view is available in Eclipse but I normally don’t use it to save me some screen space. Instead, I prefer **Ctrl+O** which shows a complete list of all the methods and fields present in the class. Press Ctrl+O again to show/hide the inherited methods for that class.

<div id="attachment_46" style="width: 456px" class="wp-caption aligncenter">
  <a href="{{site.baseurl}}/assets/uploads/2010/04/outline.png"><img class="size-full wp-image-46    " title="Show all members in a class (Ctrl+O)" alt="" src="{{site.baseurl}}/assets/uploads/2010/04/outline.png" width="446" height="311" srcset="{{site.baseurl}}/assets/uploads/2010/04/outline.png 557w, {{site.baseurl}}/assets/uploads/2010/04/outline-300x209.png 300w" sizes="(max-width: 446px) 100vw, 446px" /></a>
  
  <p class="wp-caption-text">
    Show all members in a class (Ctrl+O)
  </p>
</div>

**_Non-Navigation Features_**

**_<span style="font-style: normal; font-weight: normal;">Apart from the above there are non-navigation shortcuts which are really helpful too. One such feature is the auto-complete (<strong>Ctrl + Space</strong>). Just press Ctrl + Space after typing the first few characters of the resource and Eclipse provides you with all the options starting with those characters.</span>_**

Although, I am not a big fan of the breadcrumbs feature (**Alt+Shift+B)**, it does tell your current location with respect to a method, class and package you are working in.

<div id="attachment_48" style="width: 556px" class="wp-caption aligncenter">
  <a href="{{site.baseurl}}/assets/uploads/2010/04/bread.png"><img class="size-full wp-image-48    " title="Breadcrumbs feature" alt="" src="{{site.baseurl}}/assets/uploads/2010/04/bread.png" width="546" height="99" srcset="{{site.baseurl}}/assets/uploads/2010/04/bread.png 854w, {{site.baseurl}}/assets/uploads/2010/04/bread-300x54.png 300w" sizes="(max-width: 546px) 100vw, 546px" /></a>
  
  <p class="wp-caption-text">
    Breadcrumbs feature
  </p>
</div>

Another really helpful shortcut while refactoring is **ALT+SHIFT+T.** It finds and modifies all the appearances of a particular resource in the workspace. In particular, my favorite is **ALT+SHIFT+R** which renames all the occurrences of the particular resource. Once you are done making your changes quickly organize  all your imports using **Ctrl+Shift+O**.

<div id="attachment_44" style="width: 378px" class="wp-caption aligncenter">
  <a href="{{site.baseurl}}/assets/uploads/2010/04/refactor.png"><img class="size-full wp-image-44   " title="Refactor using Alt+Shift+R" alt="" src="{{site.baseurl}}/assets/uploads/2010/04/refactor.png" width="368" height="52" srcset="{{site.baseurl}}/assets/uploads/2010/04/refactor.png 409w, {{site.baseurl}}/assets/uploads/2010/04/refactor-300x42.png 300w" sizes="(max-width: 368px) 100vw, 368px" /></a>
  
  <p class="wp-caption-text">
    Refactor using Alt+Shift+R
  </p>
</div>

**_Take Aways_**

 ****All in all, when working with large code bases, quickly navigating to the needed resources is the key. Eclipse provides many helpful shortcuts and makes a developer more productive. The complete list of shortcuts provided by eclipse can be found by using **Ctrl+Shift+L**.

<span style="font-family: Arial; text-decoration: underline; color: #1155cc;" data-sheets-value="[null,2,&quot;https://studentshare.net/statistics&quot;]" data-sheets-userformat="[null,null,513,[null,0],null,null,null,null,null,null,null,null,0]"><a class="in-cell-link" href="https://studentshare.net/statistics" target="_blank">https://studentshare.net/statistics</a></span>

<div style="clear:both;">
  &nbsp;
</div>