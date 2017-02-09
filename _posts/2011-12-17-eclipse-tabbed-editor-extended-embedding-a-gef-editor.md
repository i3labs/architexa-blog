---
id: 232
title: Eclipse Tabbed Editor Extended.. Embedding a GEF Editor
date: 2011-12-17T19:34:27+00:00
author: Abhishek Rakshit
layout: post
guid: http://blog.architexa.com/?p=232
permalink: /2011/12/eclipse-tabbed-editor-extended-embedding-a-gef-editor/
wpbb_sync_comments:
  - 'yes'
categories:
  - Eclipse
  - Java
  - User Experience
tags:
  - eclipse
---
<!--S-ButtonZ 1.1.5 Start-->

<div style="float: left; width: 42px; padding-right: 10px; margin: 0 -52px 0 0; position: relative; left: -62px; top: 8px">
</div>

<!--S-ButtonZ 1.1.5 End-->

[<img class="alignright size-medium wp-image-233" title="MultiTabEditor" src="/assets/uploads/2011/03/MultiTabEditor-300x257.png" alt="" width="300" height="257" srcset="/assets/uploads/2011/03/MultiTabEditor-300x257.png 300w, /assets/uploads/2011/03/MultiTabEditor.png 540w" sizes="(max-width: 300px) 100vw, 300px" />](/assets/uploads/2011/03/MultiTabEditor.png)Finding the right format for users to edit and view your Eclipse plugin&#8217;s data can be tricky. Eclipse provides many different types of editors for modification of its resources. Some examples of these are the Java, Text, JSP, XML, Ant editor etc. It also provides tabbed editors like the Plug In Manifest Editor which can have multiple sub editors as tabs in one editor. A simple <a href="http://www.eclipsepluginsite.com/editors.html" target="_blank">example</a> template to extend the tabbed editor when creating a new plug-in, is provided in Eclipse by default. For our project we needed to add a compare editor and a GEF editor as sub editors. This post should help you become more familiar with creating custom tabbed editors in Eclipse.

**<!--more-->Editor Input**


  
The example provided in Eclipse uses the same EditorInput for all the sub editors. This allows the same information (from the EditorInput) to be displayed and edited differently in each sub-editor. This works fine when all the editors are closely related and a single EditorInput can take care of all the resources in different tabs. If this is not the case, for any particular editor you can provide a customized EditorInput class which implements the IEditorInput interface.

Adding a GEF editor to the MultiPageEditor is not the hard part. You can simply add a GEF editor in one of the createPage methods in the MultiPageEditor. The interesting part is getting GEF to interact correctly with the UI and user commands. Below are some issues and fixes commonly seen while working with GEF in MultiPageEditors.

**Selection Event issues**
  
When embedding a GEF editor the first issue you will face is that the selections will not work properly. This is due to the fact that the selection listeners for the GEF editor are not correctly notified of events because it is nested inside the MultiPageEditor. You can do the following to fix this issue.

a) Make the MultiPageEditor implement the ISelectionListener to be able to listen for any selection events.
  
b) Override the init method in the MultiPageEditor and add the following code to it.

`getSite().getWorkbenchWindow().getSelectionService().addSelectionListener(this);`

c) Now override the selectionChanged method and add the code to get the appropriate GEF editor and pass on the event to the GEF editor’s selectionChanged method.

`public void selectionChanged(IWorkbenchPart part, ISelection selection) {<br />
&nbsp;&nbsp;if (this.equals(getSite().getPage().getActiveEditor())) {<br />
&nbsp;&nbsp;&nbsp;&nbsp;if (getGEFEditor().equals(getActiveEditor()))<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; getGEFEditor().selectionChanged(getActiveEditor(), selection);<br />
 &nbsp;&nbsp; }<br />
}`

d) Also you might see issues with executions of your commands from the CommandStack. To get those working correctly the MultiPageEditor will also have to implement the CommandStackListener interface and you will have to override the CommandStackChanged method and call the appropriate method in the GEF editor as done for the selectionChanged method.

**Keyboard Binding Issues**
  
Another common issue when embedding GEF in tabbed editors is that keyboard shortcuts do not work properly. This can be fixed by setting the correct ActionHandlers for the GEF editor. A common way to doing this in the MultiPageEditorContributor. In the default eclipse example the method setActivePage is responsible for setting the handlers for the text editor. Similarly, you will have to check if the current page is a GEF editor and then get the ActionRegistry and set the correct handlers. Below is a code snippet to do this.

`@Override<br />
public void init(IActionBars bars) {<br />
&nbsp;&nbsp;  buildActions();<br />
 &nbsp;&nbsp; super.init(bars);<br />
}<br />
protected void buildActions() {<br />
&nbsp;&nbsp;  addAction(new SelectAllAction(activeEditorPart));<br />
 &nbsp;&nbsp; addAction(new PrintAction(activeEditorPart));<br />
&nbsp;&nbsp;  addAction(new DeleteAction((IWorkbenchPart)activeEditorPart));<br />
 &nbsp;&nbsp; addAction(new UndoAction(activeEditorPart));<br />
 &nbsp;&nbsp; addAction(new RedoAction(activeEditorPart));<br />
}<br />
protected void addAction(IAction action) {<br />
&nbsp;&nbsp;  getActionRegistry().registerAction(action);<br />
&nbsp;&nbsp;  addGlobalActionKey(action.getId());<br />
}<br />
protected void addGlobalActionKey(String key) {<br />
 &nbsp;&nbsp; globalActionKeys.add(key);<br />
}`

In the setActivePage method add the following code.

`if (part instanceof GraphicalEditor) {<br />
&nbsp;&nbsp;ActionRegistry registry = (ActionRegistry) part.getAdapter(ActionRegistry.class);<br />
&nbsp;&nbsp;for (int i = 0; i < globalActionKeys.size(); i++) {<br />
&nbsp;&nbsp;&nbsp;&nbsp;    String id = (String) globalActionKeys.get(i);<br />
&nbsp;&nbsp;&nbsp;&nbsp;    actionBars.setGlobalActionHandler(id, registry.getAction(id));<br />
&nbsp;&nbsp;  }<br />
}`

**Miscellaneous**

_Setting Editor Properties For Embedded Editor Tabs_
  
In the createPage method for the respective editor tab you can set its name and image  by getting the correct information from the EditorInput and setting it to the page. The code below shows how to put the correct image and name properties for the embedded page.

 `@Override	protected void createPages() {<br />
&nbsp;&nbsp;createPage0();<br />
&nbsp;&nbsp;createPage1();<br />
}<br />
void createPage0() {<br />
&nbsp;&nbsp;setPartName(getGEFEditor().getEditorInput().getName());<br />
&nbsp;&nbsp;setPageImage(getGEFEditor().getEditorInput().getImageDescriptor().createImage());<br />
}`

_Remove tabs if only one editor is present_
  
This is another small tip which is more of a hack to make sure that the tabs are hidden if there is only one editor present. I say this is a hack because the eclipse documentation does not specifically say that the getContainer method will return a CTabFolder. So if this is changed in the future versions this code snippet will not work. But for now if works fine for our needs.

`// Do not create second page if no diff<br />
if (getPageCount() == 1) {<br />
&nbsp;&nbsp;Composite container = getContainer();<br />
if (container instanceof CTabFolder) {<br />
&nbsp;&nbsp;((CTabFolder) container).setTabHeight(0);<br />
}<br />
` 

Using these tips you should be able to embed a GEF editor inside a MultiPageEditor without much hassle.
  
Let us know of any other points that one should keep in mind while working with MultiPageEditors and GEF editors.11111

<div style="clear:both;">
  &nbsp;
</div>