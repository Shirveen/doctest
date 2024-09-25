---
description: "Learn how to use the TRUENDO Javascript API to create custom buttons and control the Privacy Widget. Follow step-by-step instructions for various API calls. Last updated June 19, 2024.\n"
keywords:
    - TRUENDO
    - 'Javascript API'
    - 'Custom Buttons'
    - 'Privacy Widget'
    - 'Cookie Management'
    - 'Data Privacy'
canonical_url: 'https://docs.truendo.com/javascript-api'
og_title: 'Javascript API - TRUENDO Documentation'
og_description: "Follow our guide to use the TRUENDO Javascript API. Create custom buttons and control the Privacy Widget with various API calls.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-19'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Javascript API'
id: 4O6-WKD8-FTV-1H0
slug: javascript-api
isVisible: true
lastUpdated: '2024-06-21 08:19:15'
---
# <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Javascript API</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">With TRUENDO you can create custom buttons to open the Privacy Widget at certain pages.</span></span>

## <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Opening tabs with a link</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Use the following code to:</span></span>

**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Open Privacy Widget</span></span>**

`&lt;a href="javascript:Truendo.openPrivacyPanel()"&gt;Privacy Center&lt;/a&gt;`

**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Open the Privacy tab</span></span>**

`&lt;a href="javascript:Truendo.openYourRights()"&gt;Privacy Policy&lt;/a&gt;`

**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Open the Cookies tab</span></span>**

`&lt;a href="javascript:Truendo.openCookieSettings()"&gt;Cookie Manager&lt;/a&gt;`

<br />

## <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Toggle Categories</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Toggle the service categories with these functions:</span></span>

**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Social Content</span></span>**

`&lt;a href="javascript:window.Truendo.toggleContent();"&gt;Toggle Social Content&lt;/a&gt;`

**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Marketing</span></span>**

`&lt;a href="javascript:window.Truendo.toggleMarketing();"&gt;Toggle Marketing&lt;/a&gt;`

**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Statistics</span></span>**

`&lt;a href="javascript:window.Truendo.toggleStatistics();"&gt;Toggle Statistics&lt;/a&gt;`

**Additional Features**

`&lt;a href="javascript:window.Truendo.addFeatures();"&gt;Toggle Additional Features&lt;/a&gt;`

**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Preferences</span></span>**

`&lt;a href="javascript:window.Truendo.togglePreferences();"&gt;Toggle Preferences&lt;/a&gt;`

<br />

## Other API calls

**Unblocking**

This call reruns the CMP unblocking functionality based on the user's current consent choices.

```
window.Truendo.runUnblockService()
```

<br />