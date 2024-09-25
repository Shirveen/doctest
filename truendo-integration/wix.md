---
description: "Learn how to integrate TRUENDO on your Wix website with our step-by-step guide.  Set up custom code, configure placeholders for iFrames, and ensure optimal data  privacy management on your Wix site. Last updated June 18, 2024.\n"
keywords:
    - TRUENDO
    - Wix
    - Integration
    - 'iFrame Placeholder'
    - 'Data Privacy'
    - 'Cookie Management'
    - 'Website Setup'
canonical_url: 'https://docs.truendo.com/truendo-on-wix'
og_title: 'TRUENDO on Wix - TRUENDO Documentation'
og_description: "Follow our detailed guide to integrate TRUENDO with Wix. Learn to set up custom code, configure  iFrame placeholders, and manage data privacy effectively.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-18'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: Wix
id: IH9-7FD6-7SX-PPW
slug: wix
isVisible: true
lastUpdated: '2024-06-20 10:16:41'
---
# <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">TRUENDO on Wix</span></span>

## Integration

1.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Log in to Wix and click </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Site actions</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">and then </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Edit site</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">on the site to which you wish to add TRUENDO.</span></span>
2.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Click </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Site</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">in the top left of the window and then </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">My Dashboard</span></span>**
3.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Click </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Settings</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">in the menu on the left.</span></span>
4.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Under the </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Advanced Settings</span></span>** section of the window that appears <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">click on </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Custom Code</span></span>**
5.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Click the blue </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">+Add Custom Code</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">button.</span></span>
6.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">In a separate browser window log in to an existing TRUENDO account or </span></span> [<span style="color:rgb(0, 85, 187);"><span style="background-color:transparent;">Create a TRUENDO account</span></span>](https://console.truendo.com/)<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>
7.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">In the TRUENDO Console, click on </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Banner </span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">on the left sidebar then scroll down to </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Integration via Script</span></span>**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>
    
    <img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/ee08ne6mtEfxVwdplEQG.png" alt="">
    
    <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Copy your snippet, which will look something like this:</span></span>
    
    ```
    &lt;!-- TRUENDO Privacy Center --&gt;
    &lt;script id="truendoAutoBlock" type="text/javascript" src="https://cdn.priv.center/pc/truendo_cmp.pid.js" data-siteid="YOUR SITE ID"&gt;&lt;/script&gt;
    &lt;!-- End TRUENDO Privacy Center --&gt;
    ```
    
8.  Now paste this snippet back in the Wix window.
9.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Name the tool </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">TRUENDO Privacy Widget</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">or something similar.</span></span>
    
    -   <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Add the code to Pages: All Pages, load code once.</span></span>
    -   <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Place the code in: </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Head</span></span>**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">. This ensures that the Privacy Center appears every page on your website.</span></span>
10.  **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Apply</span></span>**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">. DONE!</span></span>

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/SOqxr9MzvWa4mx3KQUUu.png"></figure>

<br />

<div class="sd-callout" data-callout-type="alert"><p><strong>Important :</strong> TRUENDO only works on <a href="https://www.wix.com/upgrade/website#/" target="_blank">Wix Premium Plans</a></p></div>

## Connecting a Placeholder to a Wix iFrame

As Wix makes use of an iFrame-based component structure, integrating the TRUENDO placeholder over a privacy-relevant iFrame (YouTube, Vimeo) will not work as it would on any other CMS.

<div class="sd-callout" data-callout-type="info"><p><strong>PLEASE NOTE:</strong> While TRUENDO will autoblock a Wix video player it will not load a placeholder over it. You will have to replace the video player with an <strong>Embed HTML</strong> element containing an embedded video if you wish to have the iFrame placeholder.</p></div>

### Step 1

In the Wix Website Editor create an **Embed HTML** element which will contain the iFrame and click the **Enter Code** button. Select the **Code** radio button.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/pnGmFbSLlpRkxV9eTLm5.png"></figure>

<br />

### Step 2

Paste your iFrame content in here. Your iFrame may look something like this:

```
<iframe width="560" height="315" src="https://www.youtube.com/embed/a-youtube-video" frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

### Step 3

1.  Add the attribute `id="tru_iframe"` within the iFrame tag.
2.  Replace the `src` attribute with `data-src`
3.  Add `data-trucookiecontrol="[category]"`
4.  Add the attribute `src="https://amp.priv.center/wix-placeholder.html"` which will contain the placeholder.

Your iFrame should look like this after the above changes:

```
<iframe id="tru_iframe" width="560" height="315" src="https://amp.priv.center/wix-placeholder.html" data-src="https://www.youtube.com/embed/a-youtube-video" data-trucookiecontrol="social_content" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

### Step 4

Paste the following script directly below the iFrame tag:

```
<script>let iframe=document.getElementById("tru_iframe"),placeholderSrc=iframe.getAttribute("src"),iframeSrc=iframe.getAttribute("data-src");window.addEventListener("message",e=>{"service_enabled"==e.data?(iframe.setAttribute("src",iframeSrc),iframe.setAttribute("data-src",placeholderSrc)):"service_disabled"==e.data&&(iframe.setAttribute("src",placeholderSrc),iframe.setAttribute("data-src",iframeSrc))});</script>
```

### Step 5

Click the **Update** button to save the changes made to the element. Save your changes and Publish your site.

### Step 6

Navigate to the Wix Dashboard and click on the **Settings** option in the left hand menu.

### Step 7

Under the **Advanced** section click on Custom Code and in this window select the **Add Custom Code** button.

<figure style="width:70%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/OJuut2ZzdXP4afDRTEvg.png" width="70%"></figure>

1.  Give the custom code a memorable name like "TRUENDO Placeholder"
2.  Select the **Load code once** option under the **All pages** radio button
3.  Select the **Body - end** option

### Step 8

Paste the following script in the code snippet textbox:

```
<script defer>let timeout=1000,pageIsLoaded=!1,iframes=[];function cookieSettings(){}function sendPostMessages(e,s){e.social_content?s.forEach(e=>{e.postMessage("service_enabled","")}):e.social_content||s.forEach(e=>{e.postMessage("service_disabled","")})}window.addEventListener("TruendoCookieControl",function(e){let s=e.detail;pageIsLoaded?pageIsLoaded&&sendPostMessages(s,iframes):(setTimeout(()=>{sendPostMessages(s,iframes=Array.from(window.frames))},timeout),pageIsLoaded=!0)});</script>
```

Click **Apply** and you should be done!

<div class="sd-callout" data-callout-type="alert"><p><strong>Important :</strong> The HTML Embed may take longer to load than expected on the webpage which can affect the behavior of the placeholder. To accommodate for the delay you can adjust the <code>timeout</code> value in the above script. It should be no shorter than 500ms. Wix does provide a metric that measures the <strong>Site speed</strong>, you may adjust the value according to that time.</p></div>

<br />