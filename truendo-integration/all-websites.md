---
description: "Enable your website to automatically find and permit/block categorized cookies with no coding.  Follow our step-by-step guide to create a TRUENDO account, integrate scripts, and manage  cookie settings. Last updated June 18, 2024.\n"
keywords:
    - TRUENDO
    - 'All Websites'
    - 'Cookie Management'
    - Integration
    - Auto-blocking
    - 'Script Integration'
    - 'Data Privacy'
canonical_url: 'https://docs.truendo.com/all-websites'
og_title: 'All Websites - TRUENDO Documentation'
og_description: "Learn how to set up TRUENDO on any website to automatically manage cookies without coding.  Step-by-step integration guide included.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-18'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'All Websites'
id: 6FY-XTZ-IMX-OWH
slug: all-websites
isVisible: true
lastUpdated: '2024-06-20 09:55:22'
---
# All Websites<br />

## <span style="color:rgba(77,77,77,1);"><span style="background-color:rgb(255, 255, 255);">With Auto-blocking</span></span>

Enable your website to automatically find and permit/block categorized cookies with no coding.

<iframe src="https://www.youtube.com/embed/KyXBnDlnf9U?showinfo=0" frameborder="0" allowfullscreen="true" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" width="100%"></iframe>

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 1:</span></span>

[<span style="color:rgb(0, 85, 187);"><span style="background-color:transparent;">Create a TRUENDO account</span></span>](https://console.truendo.com/) or log in to an existing one.

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 2:</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">In the TRUENDO Console, click on </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Banner </span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">on the left sidebar then scroll down to </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Integration via Script</span></span>**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>

<img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/ee08ne6mtEfxVwdplEQG.png" alt="">

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Copy your snippet, which will look something like this:</span></span>

```
<!-- TRUENDO Privacy Center -->
<script id="truendoAutoBlock" type="text/javascript" src="https://cdn.priv.center/pc/truendo_cmp.pid.js" data-siteid="YOUR SITE ID"></script>
<!-- End TRUENDO Privacy Center -->
```

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 3:</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Paste the snippet in the </span></span> `&lt;head&gt;` <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">as the </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">very first script</span></span>**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">, on the page section of your website. See this example below:</span></span>

```html
<html>
<head>
<!-- TRUENDO Privacy Center -->
<script id="truendoAutoBlock" type="text/javascript" src="https://cdn.priv.center/pc/truendo_cmp.pid.js" data-siteid="YOUR SITE ID"></script>
<!-- End TRUENDO Privacy Center -->
<!-- Every other script -->
<script>...</script>
</head>
<body> […] </body>
</html>
```

**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Save your changes.</span></span>**

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">You are done.</span></span>

## <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Without Auto-blocking</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Follow the same steps but replace your script with the following one. Remember to replace your Site ID with the one of your project.</span></span>

```html
<!-- TRUENDO Privacy Center -->
<script async="" id="truendoPrivacyPanel" type="text/javascript" src="https://cdn.priv.center/pc/app.pid.js" data-siteid="YOUR SITE ID"></script>
<!-- End TRUENDO Privacy Center -->
```

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Connect your cookies as explained </span></span> [<span style="color:rgb(0, 85, 187);"><span style="background-color:rgb(255, 255, 255);">here</span></span>](http:#?target=VZS-XH3U-7F7-3BB)

<br />