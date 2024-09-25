---
description: "Learn how to integrate TRUENDO on your AMP pages with our step-by-step guide.  Insert the TRUENDO code snippet, configure consent settings, and ensure optimal  data privacy management on your AMP site. Last updated June 18, 2024.\n"
keywords:
    - TRUENDO
    - AMP
    - Integration
    - 'Consent Management'
    - 'Data Privacy'
    - 'Cookie Management'
    - 'Website Setup'
canonical_url: 'https://docs.truendo.com/truendo-on-amp'
og_title: 'TRUENDO on AMP - TRUENDO Documentation'
og_description: "Follow our detailed guide to integrate TRUENDO with AMP. Learn to insert and configure  the TRUENDO code snippet for enhanced data privacy on your AMP pages.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-18'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: AMP
id: DYK-6NIV-J0M-RUS
slug: amp
isVisible: true
lastUpdated: '2024-06-20 11:19:57'
---
# <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">TRUENDO on AMP</span></span>

## Integration

### Step 1:

Paste the script below inside the head of your AMP page.

This script enables us to use TRUENDO in AMP.

```
<script async custom-element="amp-consent" src="https://cdn.ampproject.org/v0/amp-consent-0.1.js"</script>
```

### Step 2:

Paste this code block inside the body of the html of your AMP page.

```
    <amp-consent id="truendo" layout="nodisplay">
        <script type="application/json">{
          "consentInstanceId": "truendo",
          "consentRequired": "remote",
          "checkConsentHref": "https://prod-fra.truendo.com/consent/public/amp/check",
          "promptUISrc": "https://amp.priv.center/amp.html?tru-type=amp&site-id={{site-id}}"}</script>
      </amp-consent>
```

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 3</span></span>:

Replace {{site-id}} with your Site-ID

This is how TRUENDO will identify you.

```
    <amp-consent id="truendo" layout="nodisplay">
        <script type="application/json">
        {
          "consentInstanceId": "truendo",
          "consentRequired": "remote",
          "checkConsentHref": "https://prod-fra.truendo.com/consent/public/amp/check",
          "promptUISrc": "https://amp.priv.center/amp.html?tru-type=amp&site-id=20ee-r086-40g-8ajee-35c9op085cf0"
        }
        </script>
      </amp-consent>
```

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">The Privacy Widget should now appear on your AMP page.</span></span>

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 4</span></span>:

Optional

Example of a button that enables users to make changes to their cookie preferences.

```
<div id="post-consent-ui">
<button on="tap:truendo.prompt()">Update Consent</button>
</div>
```

Add this key, value pair inside the script tag under "promptUISrc": "post-consent-ui".

```
    <amp-consent id="truendo" layout="nodisplay">
        <script type="application/json">{
          "consentInstanceId": "truendo",
          "consentRequired": "remote",
          "checkConsentHref": "https://prod-fra.truendo.com/consent/public/amp/check",
          "promptUISrc": "https://amp.priv.center/amp.html?tru-type=amp&site-id=20ee-r086-40g-8ajee-35c9op085cf0",
          "postPromptUI": "post-consent-ui"
        }
      </script>
      </amp-consent>
```

These changes will allow users to change their preferences.<br />

## How TRUENDO handles the TC string in an AMP page?

TRUENDO sends the TC string in a postMessage to the parent page (AMP).

The parent page (AMP) listens to this postMessage and retrieves the data.<br />

Sample data object recieved by postMessage:

```
        {
          type: "consent-response",
          action: "accept",
          info:{
            'clientConfig': '*',
            'consentStateValue': 'accepted',
            'consentString': 'CPn3nn3nTPEENC5CgAAH',
            },
          consentMetadata:{
            "consentStringType": 2,
            "gdprApplies": true,
           }
        }
```

## How to retrieve the TC string in an AMP page?

You can listen to the postMessage TRUENDO makes in your AMP page.<br />

## **<span style="color:rgb(26, 26, 26) !important;"><span style="background-color:rgb(255, 255, 255);">Need help?</span></span>**

<span style="color:rgb(10, 10, 10);"><span style="background-color:rgb(255, 255, 255);">For more information regarding AMP please visit </span></span> [https://amp.dev/](https://amp.dev/)<br />
<br />