---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2"
path: ""
category: api
id: "nav"
title: "Nav"
header_sub_title: "Class in module "
doc: "Nav"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/navigation/"
angular_controller: APIDemoCtrl 
---









<h1 class="api-title">
<a class="anchor" name="nav" href="#nav"></a>

Nav






</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/2.0//ionic/components/nav/nav.ts#L8">
Improve this doc
</a>






<p><em>For a quick walkthrough of navigation in Ionic, check out the
<a href="../../../../components/#navigation">Navigation section</a> of the Component
docs.</em></p>
<p>Nav is a basic navigation controller component.  As a subclass of NavController
you use it to navigate to pages in your app and manipulate the navigation stack.
Nav automatically animates transitions between pages for you.</p>
<p>For more information on using navigation controllers like Nav or <a href="../../Tabs/Tab/">Tab</a>,
take a look at the <a href="../NavController/">NavController API reference</a>.</p>
<p>You must set a root page (where page is any <a href="../../config/Page/">@Page</a>
component) to be loaded initially by any Nav you create, using
the &#39;root&#39; property:</p>


<h2><a class="anchor" name="Component" href="#Component"></a>Component</h2>
<h3>selector: <code>ion-nav</code></h3>
<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<pre><code class="lang-ts">import {GettingStartedPage} from &#39;getting-started&#39;;
@App({
  template: `&lt;ion-nav [root]=&quot;rootPage&quot;&gt;&lt;/ion-nav&gt;`
})
class MyApp {
  constructor(){
    this.rootPage = GettingStartedPage;
  }
}
</code></pre>
<p><h2 id="back_navigation">Back navigation</h2>
If a <a href="../NavController/#creating_pages">page</a> you navigate to has a <a href="../NavBar/">NavBar</a>,
Nav will automatically add a back button to it if there is a page
before the one you are navigating to in the navigation stack.</p>
<p>Additionally, specifying the <code>swipeBackEnabled</code> property will allow you to
swipe to go back:</p>
<pre><code class="lang-html">&lt;ion-nav swipeBackEnabled=&quot;false&quot; [root]=&quot;rootPage&quot;&gt;&lt;/ion-nav&gt;
</code></pre>
<p>Here is a diagram of how Nav animates smoothly between pages:</p>
<div class="highlight less-margin">
  <pre>
                          +-------+
                          |  App  |
                          +---+---+
                          &lt;ion-app&gt;
                              |
                 +------------+-------------+
                 |   Ionic Nav Controller   |
                 +------------+-------------+
                          &lt;ion-nav&gt;
                              |
                              |
            Page 3  +--------------------+                     LoginPage
          Page 2  +--------------------+ |
        Page 1  +--------------------+ | |              +--------------------+
                | | Header           |&lt;-----------------|       Login        |
                +--------------------+ | |              +--------------------+
                | | |                | | |              | Username:          |
                | | |                | | |              | Password:          |
                | | |  Page 3 is     | | |              |                    |
                | | |  only content  | | |              |                    |
                | | |                |&lt;-----------------|                    |
                | | |                | | |              |                    |
                | | |                | | |              |                    |
                | +------------------|-+ |              |                    |
                | | Footer           |-|-+              |                    |
                | +------------------|-+                |                    |
                +--------------------+                  +--------------------+

          +--------------------+    +--------------------+    +--------------------+
          | Header             |    | Content            |    | Content            |
          +--------------------+    |                    |    |                    |
          | Content            |    |                    |    |                    |
          |                    |    |                    |    |                    |
          |                    |    |                    |    |                    |
          |                    |    |                    |    |                    |
          |                    |    |                    |    |                    |
          |                    |    |                    |    |                    |
          |                    |    |                    |    |                    |
          |                    |    |                    |    |                    |
          |                    |    +--------------------+    |                    |
          |                    |    | Footer             |    |                    |
          +--------------------+    +--------------------+    +--------------------+

  </pre>
</div>



<!-- @property tags -->



<!-- instance methods on the class -->
<!-- input methods on the class -->
<h2><a class="anchor" name="input-properties" href="#input-properties"></a>Input Properties</h2>
<table class="table param-table" style="margin:0;">
  <thead>
    <tr>
      <th>Attr</th>
      <th>Type</th>
      <th>Details</th>
    </tr>
  </thead>
  <tbody>
    
    <tr>
      <td>root</td>
      <td><code>Page</code></td>
      <td><p> The Page component to load as the root page within this nav.</p>
</td>
    </tr>
    
    <tr>
      <td>swipeBackEnabled</td>
      <td><code>boolean</code></td>
      <td><p> Whether it&#39;s possible to swipe-to-go-back on this nav controller or not.</p>
</td>
    </tr>
    
  </tbody>
</table><!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='/docs/v2/components#navigation'>Navigation Component Docs</a><!-- end content block -->


<!-- end body block -->

