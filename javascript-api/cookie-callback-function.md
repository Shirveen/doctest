---
description: "Learn how to add custom code when cookie settings are changed using the TRUENDO Cookie Callback Function. Follow step-by-step examples to integrate callback functions and event listeners. Last updated June 19, 2024.\n"
keywords:
    - TRUENDO
    - 'Cookie Callback Function'
    - 'Custom Code'
    - 'Event Listener'
    - 'Cookie Settings'
    - 'Data Privacy'
canonical_url: 'https://docs.truendo.com/cookie-callback-function'
og_title: 'Cookie Callback Function - TRUENDO Documentation'
og_description: "Follow our guide to add custom code when cookie settings are changed using the TRUENDO Cookie Callback Function. Integrate callback functions and event listeners effectively.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-19'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Cookie Callback Function'
id: 0BY-JNNR-11P-2HQ
slug: cookie-callback-function
isVisible: true
lastUpdated: '2024-06-21 08:37:37'
---
# <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Cookie Callback Function</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">You can add custom code when cookie settings are changed either by creating a global function with the name </span></span> `TruendoCookieControlCallback` or by adding a listener for the `TruendoCookieControl` event to `window`.

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Callback example</span></span>

```html
<script type="text/javascript">
  function TruendoCookieControlCallback(cookieSettings) {
    if (cookieSettings.ack) {
      console.log('Cookie dialog acknowledged');
    }
    if (cookieSettings.necessary) {
      console.log('Necessary cookies enabled.');
    }
    if (cookieSettings.preferences) {
      console.log('Preference cookies enabled.');
    }
    if (cookieSettings.statistics) {
      console.log('Statistics cookies enabled.');
    }
    if (cookieSettings.marketing) {
      console.log('Marketing cookies enabled.');
    }
    if (cookieSettings.social_content) {
      console.log('Social Content cookies enabled.');
    }
  }
</script>
```

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Event listener example</span></span>

```html
<script type="text/javascript">
  window.addEventListener('TruendoCookieControl', function (event) {
    // cookie settings accessible via event.detail
    var cookieSettings = event.detail;

    if (cookieSettings.ack) {
      console.log('Cookie dialog acknowledged');
    }
    if (cookieSettings.necessary) {
      console.log('Necessary cookies enabled.');
    }
    if (cookieSettings.preferences) {
      console.log('Preference cookies enabled.');
    }
    if (cookieSettings.statistics) {
      console.log('Statistics cookies enabled.');
    }
    if (cookieSettings.marketing) {
      console.log('Marketing cookies enabled.');
    }
        if (cookieSettings.social_content) {
      console.log('Social Content cookies enabled.');
    }
   });
</script>
```

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Cookie Settings object</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">In addition to receiving the cookie settings within a callback or event listener, you can access the cookie settings at any time via the read-only </span></span> `Truendo.cookieSettings` property.

## <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Microsoft Dynamics</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Please add the following script below your Microsoft Dynamics script.</span></span>

> <div class="sd-callout" data-callout-type="alert"><strong>Important:</strong> For this to work properly Microsoft Dynamics hast to be added to a category other than Marketing (like Statistics)</div>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Find more Information in the Microsoft Dynamics Documentation:<br></span></span>[<span style="color:rgb(0, 85, 187);"><span style="background-color:transparent;">Microsoft Dynamics Docs</span></span>](https://docs.microsoft.com/en-us/dynamics365/marketing/cookies)

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Callback example</span></span>

```html
<script>
  function TruendoCookieControlCallback(cookieSettings) {
    if (cookieSettings.necessary) {
     // Run code here that should if this category is opted in
    }
    if (cookieSettings.preferences) {
     // Run code here that should if this category is opted in
    }
    if (cookieSettings.statistics) {
     // Run code here that should if this category is opted in
    }
    if (cookieSettings.marketing) {
      MsCrmMkt.reconfigureTracking({Anonymize: false});
    } else { // else command to run code when the user does not accept
      MsCrmMkt.reconfigureTracking({Anonymize: true});
    }
    if (cookieSettings.social_content) {
     // Run code here that should if this category is opted in
    }
  }
</script>
```

<br />