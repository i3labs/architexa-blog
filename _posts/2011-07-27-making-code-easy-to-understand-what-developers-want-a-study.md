---
id: 198
title: 'Making Code Easy to Understand &#8211; What Developers Want (a study)'
date: 2011-07-27T08:10:01+00:00
author: Vineet Sinha
layout: post
guid: http://blog.architexa.com/?p=198
permalink: /2011/07/making-code-easy-to-understand-what-developers-want-a-study/
wpbb_sync_comments:
  - 'yes'
categories:
  - 'Documentation &amp; Communication'
  - Understanding Developers
  - User Experience
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img src="{{site.baseurl}}/assets/uploads/2011/05/graph2-300x178.png" alt="" title="graph2" width="300" height="178" class="alignright size-medium wp-image-253" srcset="{{site.baseurl}}/assets/uploads/2011/05/graph2-300x178.png 300w, {{site.baseurl}}/assets/uploads/2011/05/graph2-1024x608.png 1024w, {{site.baseurl}}/assets/uploads/2011/05/graph2.png 1367w" sizes="(max-width: 300px) 100vw, 300px" />]({{site.baseurl}}/assets/uploads/2011/05/graph2.png)What exactly makes a codebase easy to understand; the documentation or the tools that you use? In our effort to help developers who are working with large codebases, we conducted a survey (see [details](http://blog.architexa.com/2011/02/making-cool-ideas-happen-studying-our-users-and-software-immigrants/ "A Study of How Developers Understand New Codebases") and [highlights](http://blog.architexa.com/2011/07/a-detailed-study-on-understanding-code/ "A Detailed Study on Understanding Code")) to find out what techniques developers use to better understand code.
  
<!--more-->


  
One of the major questions that we had was that we wanted to know which documentation techniques were being used effectively (by the average Open Source project). 

We found that there was a consistent opinion of most developers saying that projects were effectively using Javadoc, Code examples, and Articles on using Code. Other methods of documentation such as Articles on the Code Architecture, Diagrams of code components, Mailing list, Manual, and Test cases seemed to either be less useful for helping understanding or were not consistently used well. The responses:

<center>
  </p> 
  
  <div>
    <table border="1" cellspacing="0" cellpadding="3">
      <tr>
        <th>
          Documentation Technique
        </th>
        
        <th>
          Saying<br />Effectively<br />Used
        </th>
      </tr>
      
      <tr>
        <td>
          Javadoc
        </td>
        
        <td>
          45%
        </td>
      </tr>
      
      <tr>
        <td>
          Code examples
        </td>
        
        <td>
          38%
        </td>
      </tr>
      
      <tr>
        <td>
          Articles describing using code
        </td>
        
        <td>
          37%
        </td>
      </tr>
      
      <tr>
        <td>
          Articles describing code architecture
        </td>
        
        <td>
          18%
        </td>
      </tr>
      
      <tr>
        <td>
          Code structure, pattern usage, etc
        </td>
        
        <td>
          14%
        </td>
      </tr>
      
      <tr>
        <td>
          Diagrams of code components
        </td>
        
        <td>
          4%
        </td>
      </tr>
      
      <tr>
        <td>
          Mailing list
        </td>
        
        <td>
          4%
        </td>
      </tr>
      
      <tr>
        <td>
          Test cases
        </td>
        
        <td>
          1%
        </td>
      </tr>
    </table>
  </div>
  
  <p>
    </center>
  </p>
  
  <p>
    Knowing what is used effectively is important to us; we need to make sure that our <a href="http://www.architexa.com" title="Architexa">code understanding</a> tools support these practices.
  </p>
  
  <p>
    We further asked developers what kind of resources they wish to have for this purpose. We wanted to find out what exactly is lacking with the currently available tools and why are they not as effective as the developers hope them to be.
  </p>
  
  <p>
    According to the results of the survey, 45% of developers wish they had access to more articles explaining the code architecture and 42% wanted more diagrams of the code. More detailed responses are below:
  </p>
  
  <p>
    <center>
      </p> 
      
      <div>
        <table border="1" cellspacing="0" cellpadding="3">
          <tr>
            <th>
              Documentation Technique
            </th>
            
            <th>
              Want to Have
            </th>
          </tr>
          
          <tr>
            <td>
              Articles describing code architecture
            </td>
            
            <td>
              45%
            </td>
          </tr>
          
          <tr>
            <td>
              Diagrams of code components
            </td>
            
            <td>
              42%
            </td>
          </tr>
          
          <tr>
            <td>
              Articles describing using code
            </td>
            
            <td>
              33%
            </td>
          </tr>
          
          <tr>
            <td>
              Code Examples
            </td>
            
            <td>
              29%
            </td>
          </tr>
          
          <tr>
            <td>
              Javadocs
            </td>
            
            <td>
              24%
            </td>
          </tr>
        </table>
      </div>
      
      <p>
        </center>
      </p>
      
      <p>
        The message was clear. While developers are getting a lot of detailed information about projects (Javadoc, examples, articles describing code use), <strong>they are lacking the high level overviews that would allow them to better understand a new project or codebase at a glance.</strong> It does not matter whether this information comes in the form of a diagram or an article describing a codebase as long as it is still helpful to developers and allows them to understand new code quickly and easily.
      </p>
      
      <p>
        Architexa has taken these results to heart and we are resolved to provide a tool that can provide high level overviews in the form of both diagrams and architectural explanations as well as more common documentation such as Javadoc and code examples.
      </p>
      
      <div style="clear:both;">
        &nbsp;
      </div>