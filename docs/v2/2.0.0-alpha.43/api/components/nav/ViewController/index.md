---
layout: "v2_fluid/docs_base"
version: "2.0.0-alpha.43"
versionHref: "/docs/v2/2.0.0-alpha.43"
path: ""
category: api
id: "{{ViewController | slugify}}"
title: "ViewController"
header_sub_title: "Class in module "
doc: "ViewController"
docType: "class"

---




<div class="improve-docs">
<a href='http://github.com/driftyco/ionic2/tree/master/ionic/components/nav/view-controller.ts#L0'>
View Source
</a>
&nbsp;
<a href='http://github.com/driftyco/ionic2/edit/master/ionic/components/nav/view-controller.ts#L0'>
Improve this doc
</a>
</div>





<h1 class="api-title">


ViewController






</h1>






<!-- description -->
<h2>Description</h2>

<p>Access various features and information about the current view</p>

<!-- @usage tag -->

<h2>Usage</h2>

<pre><code class="lang-ts">import {Page, ViewController} from &#39;ionic/ionic&#39;;
@Page....
export class MyPage{
 constructor(viewCtrl: ViewController){
   this.viewCtrl = viewCtrl;
 }
}
</code></pre>




<!-- @property tags -->


<!-- methods on the class -->

<h2>Methods</h2>

<div id="enableBack"></div>

<h3>
<code>enableBack(Check)</code>
  

</h3>

Check to see if you can go back in the navigation stack


<table class="table" style="margin:0;">
  <thead>
    <tr>
      <th>Param</th>
      <th>Type</th>
      <th>Details</th>
    </tr>
  </thead>
  <tbody>
    
    <tr>
      <td>
        Check
        
        
      </td>
      <td>
        
  <code>boolean</code>
      </td>
      <td>
        <p>whether or not you can go back from this page</p>

        
      </td>
    </tr>
    
  </tbody>
</table>





* Returns: 
  <code>boolean</code> Returns if it's possible to go back from this Page.




<div id="index"></div>

<h3>
<code>index()</code>
  

</h3>

You can find out the index of the current view is in the current navigation stack

```typescript
 export class Page1 {
   constructor(view: ViewController){
     this.view = view;
     // Just log out the index
     console.log(this.view.index);
   }
 }
```







* Returns: 
  <code>Number</code> Returns the index of this page within its NavController.




<div id="isRoot"></div>

<h3>
<code>isRoot()</code>
  

</h3>








* Returns: 
  <code>boolean</code> Returns if this Page is the root page of the NavController.




<div id="hasNavbar"></div>

<h3>
<code>hasNavbar()</code>
  

</h3>

You can find out of the current view has a Navbar or not. Be sure to wrap this in an `onPageWillEnter` method in order to make sure the view has rendered fully.

```typescript
export class Page1 {
 constructor(view: ViewController) {
   this.view = view
 }
 onPageWillEnter(){
   console.log('Do we have a Navbar?', this.view.hasNavbar());
 }
}
```







* Returns: 
  <code>boolean</code> Returns a boolean if this Page has a navbar or not.




<div id="setBackButtonText"></div>

<h3>
<code>setBackButtonText(backButtonText)</code>
  

</h3>

You can change the text of the back button on a view-by-view basis.

```ts
export class MyClass{
 constructor(viewCtrl: ViewController){
   this.viewCtrl = viewCtrl
 }
 onPageWillEnter() {
   this.viewCtrl.setBackButtonText('Previous');
 }
}
```
Make sure you use the view events when calling this method, otherwise the back-button will not have been created



<table class="table" style="margin:0;">
  <thead>
    <tr>
      <th>Param</th>
      <th>Type</th>
      <th>Details</th>
    </tr>
  </thead>
  <tbody>
    
    <tr>
      <td>
        backButtonText
        
        
      </td>
      <td>
        
  <code>string</code>
      </td>
      <td>
        <p>Set the back button text.</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="showBackButton"></div>

<h3>
<code>showBackButton(Set)</code>
  

</h3>

Set if the back button for the current view is visible or not. Be sure to wrap this in `onPageWillEnter` to make sure the has been compleltly rendered.


<table class="table" style="margin:0;">
  <thead>
    <tr>
      <th>Param</th>
      <th>Type</th>
      <th>Details</th>
    </tr>
  </thead>
  <tbody>
    
    <tr>
      <td>
        Set
        
        
      </td>
      <td>
        
  <code>boolean</code>
      </td>
      <td>
        <p>if this Page&#39;s back button should show or not.</p>

        
      </td>
    </tr>
    
  </tbody>
</table>






<!-- related link --><!-- end content block -->


<!-- end body block -->

