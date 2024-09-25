---
description: "Learn about Google Consent Mode V2, an enhanced tool by Google to help website owners manage consent for Google services in compliance with data privacy regulations. Follow step-by-step instructions to enable Consent Mode V2 with or without Google Tag Manager (GTM). Last updated July 5, 2024.\n"
keywords:
    - 'Google Consent Mode V2'
    - TRUENDO
    - 'Data Privacy'
    - 'Google Analytics'
    - 'Google Ads'
    - 'Consent Management'
canonical_url: 'https://docs.truendo.com/guides/google-consent-mode-v2'
og_title: 'Google Consent Mode V2 - TRUENDO Documentation'
og_description: "Discover how to implement Google Consent Mode V2 with TRUENDO. Manage consent for Google services and ensure compliance with data privacy regulations.\n"
author: 'TRUENDO Team'
date_modified: '2024-07-05'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: Index
id: L42-H08X-8J0-NOG
slug: index
isVisible: true
lastUpdated: '2024-07-24 06:42:25'
---
# Google Consent Mode V2

Google consent mode V2 although still in beta phase was made mandatory in March of 2024 by Google when using Google services such as Google Ads, Floodlight, Google analytics, etc

<br />

## What is it?

Google Consent Mode V2 is an enhanced version of Google's Consent Mode, a tool designed to help website owners manage consent for Google services in compliance with data privacy regulations. It allows websites to adjust the behavior of Google tags based on the consent status of their users. This ensures that no personal data is collected or stored without proper user consent. With Version 2, improvements have been made to enhance flexibility, usability, and integration with other consent management platforms.

It has two modes of operation **Basic** Consent Mode and **Advanced** Consent Mode, carry on reading or click [here](#whats-the-difference-between-basic-and-advanced-consent-mode) to find out the key differences between the two.

<br />

## When do I use it?

-   **When Using Google Services:** If you are utilizing Google Analytics, Google Ads, or other Google services that collect user data, Consent Mode V2 allows these services to operate in a way that respects user consent choices.
-   **Complying with Data Privacy Laws:** If your website operates in regions with strict data privacy regulations (such as GDPR in the EU or CCPA in California), Consent Mode helps ensure compliance by managing how Google tags behave based on user consent.
    
    <br />
    

## How do I activate/enable it?

Generally speaking Google services (including Google Analytics) are incorporated into a website by use of Google tags which are usually managed by Google Tag Manager (GTM) where Consent Mode can be enabled via the GTM interface. The TRUENDO CMP can also be integrated within GTM. For more info on enabling Consent mode via GTM click [here](http:#?target=0B2-VIYU-VYG-YBL).<br />
<br />
It is however possible to use Consent Mode V2 without GTM. This is only possible when **the only Google Service a website uses is Google Analytics** , this can be done by adding specific code to a website's HTML for more info click [here](http:#?target=VYR-Y9QX-5VO-ULK).

<br />

## Whats The Difference between Basic and Advanced Consent Mode?

In a nutshell, with **Advanced Consent Mode** Google tags always fire regardless of consent choice but communicate non privacy relevant data to Google whereas in **Basic Consent Mode** no tag firing occurs without consent.

Implementation differs between the two in that Advanced Consent Mode, despite its name, requires fewer steps than Basic Consent Mode. Basic consent mode does however offer more granular control over tag behaviour.<br />
<br />
The tables below summarize the key differences between the two modes.

<table><tbody><tr><td><p><strong>Feature</strong></p></td><td><p><strong>Basic consent mode</strong></p></td><td><p><strong>Advanced consent mode</strong></p></td></tr><tr><td style="background-color: rgb(242, 242, 242);"><p><em><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Tag loading</span></span></em></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Blocked until user interaction with a consent banner.</span></span></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Loads with defaults set to denied, unless configured otherwise.</span></span></p></td></tr><tr><td style="background-color: rgb(255, 255, 255);"><p><em><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">Data transmission</span></span></em></p></td><td style="background-color: rgb(255, 255, 255);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">No data is sent before a user consents -&nbsp;not even the default consent status.</span></span></p></td><td style="background-color: rgb(255, 255, 255);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">When consent is denied, consent state and cookieless pings are sent.<br>When consent is granted, cookies are written and all measurement data is sent.</span></span></p></td></tr><tr><td style="background-color: rgb(242, 242, 242);"><p><em><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Consent states</span></span></em></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Set after user interaction.</span></span></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Defaults set to denied, unless configured otherwise;&nbsp; updates based on user choice.</span></span></p></td></tr><tr><td style="background-color: rgb(255, 255, 255);"><p><em><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">Tag behavior after user interaction</span></span></em></p></td><td style="background-color: rgb(255, 255, 255);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">Loads and executes consent mode APIs only when a user grants consent.</span></span></p></td><td style="background-color: rgb(255, 255, 255);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">Adjusts tag behavior based on user consent choice.</span></span></p></td></tr><tr><td style="background-color: rgb(242, 242, 242);"><p><em><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Conversion modeling</span></span></em></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">General model (less detailed modeling).</span></span></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Advertiser-specific model (more detailed modeling).</span></span></p></td></tr></tbody></table>

taken from: https://support.google.com/google-ads/answer/10000067?hl=en

<br />

#### What does this mean for Google based tags (GA4, Ads, Floodlight, etc)?

<table><tbody><tr><td><p><strong>Basic consent mode</strong></p></td><td><p><strong>Advanced consent mode</strong></p></td></tr><tr><td style="background-color: rgb(242, 242, 242);"><p><span style="background-color:rgb(242, 242, 242);">No Google tags will fire if set up correctly</span></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="background-color:rgb(242, 242, 242);">Google tags will fire based on trigger</span></p></td></tr><tr><td style="background-color: rgb(255, 255, 255);"><p><span style="background-color:rgb(255, 255, 255);">There should be no network traffic in respect of this</span></p></td><td style="background-color: rgb(255, 255, 255);"><p><span style="background-color:rgb(255, 255, 255);">Default consent states will be set and communicated, a network request (gcs event) confirming this will be present in your network traffic, see </span><a href="http:#?target=JRI-GCBU-8GF-ZHS" target="_self"><span style="background-color:rgb(255, 255, 255);">here</span></a><span style="background-color:rgb(255, 255, 255);"> for more info on these</span></p></td></tr><tr><td style="background-color: rgb(242, 242, 242);"><p><span style="background-color:rgb(242, 242, 242);">No privacy based data will be collected until relevant consent is granted</span></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="background-color:rgb(242, 242, 242);">No privacy based data will be collected until relevant consent is granted</span></p></td></tr></tbody></table>

<br />

## Which one should I use?

This is ultimately up to you and your specific use case, the legislation in effect in your area or simply personal preference.

It is worth noting that in both cases no privacy relevant data is communicated to Google without consent.

<br />

Please click the implementation method that you would like to use below to see a full step by step guide on how to get Consent Mode V2 up and running with TRUENDO:<br />

<div class="sd-callout" data-callout-type="alert">Remember if you only use <strong>Google Analytics but integrate it using GTM then you must use the first option</strong></div>

-   [Using GTM](http:#?target=0B2-VIYU-VYG-YBL)
-   [Without GTM](http:#?target=VYR-Y9QX-5VO-ULK) **(site only uses Google Analytics, not integrated by GTM)**

<br />