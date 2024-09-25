---
description: "Learn how to manually configure scripts to be controlled by TRUENDO. Add the necessary attributes to ensure scripts are not autoblocked and run only with user consent. Last updated June 21, 2024.\n"
keywords:
    - TRUENDO
    - Scripts
    - 'Script Configuration'
    - 'Cookie Management'
    - 'Data Privacy'
    - 'User Consent'
canonical_url: 'https://docs.truendo.com/scripts'
og_title: 'Scripts - TRUENDO Documentation'
og_description: "Follow our guide to configure scripts for TRUENDO control. Ensure scripts are not autoblocked and run only with user consent.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-21'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: Scripts
id: IAX-IEU-9UP-WCT
slug: scripts
isVisible: true
lastUpdated: '2024-06-21 08:12:03'
---
# Scripts

<div class="sd-callout" data-callout-type="alert"><p>This section is <strong>for users who wish to manually control blocking</strong>, TRUENDO uses <strong>autoblocking by default</strong> and this is <strong>not required for users who do not want to use manual blocking</strong>.</p></div>

## <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">How to Block Cookies</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">You will have to add two attributes to every script in your website that needs to be controlled by TRUENDO.</span></span>

The first attribute `truendo` is set to `"true"`, thus ensuring that it is not autoblocked by TRUENDO.

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Second we set the </span></span> `type` attribute to `"text/plain"`. This way the script is not running before the user accepts it.

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">The third attribute is </span></span> `data-trucookiecontrol`. This attribute has to be set to the corresponding category. For example `"statistics"`. When both are in the script it could look something like this:

```html
<script truendo="true" data-trucookiecontrol="statistics" src="[...]" type="text/plain"></script>
```

[click here](http:#?target=0EB-94M4-TBP-GIU) for a list of technical category names.

> <div class="sd-callout" data-callout-type="info"><p><strong>Important Note:</strong> Scripts that fall under the necessary category should not be changed as these can run without consent.</p></div>

<br />