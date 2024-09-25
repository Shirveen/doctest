---
description: "Explore the key differences between Advanced and Basic Consent Modes in TRUENDO. Understand how each mode impacts tag loading, data transmission, consent states, and conversion modeling to ensure compliance and optimized performance. Last updated June 19, 2024.\n"
keywords:
    - TRUENDO
    - 'Consent Mode'
    - 'Advanced Consent'
    - 'Basic Consent'
    - 'Data Privacy'
    - 'Tag Loading'
    - 'Conversion Modeling'
canonical_url: 'https://docs.truendo.com/advanced-vs-basic-consent-mode'
og_title: 'Advanced vs Basic Consent Mode - TRUENDO Documentation'
og_description: "Learn the differences between Advanced and Basic Consent Modes in TRUENDO. Ensure compliance and optimize performance by understanding tag loading, data transmission, and consent states.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-19'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Advanced vs&#46; Basic Consent mode'
id: CJC-E3MU-14S-M8L
slug: advanced-vs-dot-basic-consent-mode
isVisible: true
lastUpdated: '2024-06-27 08:49:24'
---
# Advanced vs Basic Consent Mode

Before proceding we advise you determine which best suits you. To do this we provide a quick reference guide for more detailed info please consult the consent mode documentation.

<br />

## Overview

<table><tbody><tr><td><p><strong>Feature</strong></p></td><td><p><strong>Basic consent mode</strong></p></td><td><p><strong>Advanced consent mode</strong></p></td></tr><tr><td style="background-color: rgb(242, 242, 242);"><p><em><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Tag loading</span></span></em></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Blocked until user interaction with a consent banner.</span></span></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Loads with defaults set to denied, unless configured otherwise.</span></span></p></td></tr><tr><td style="background-color: rgb(255, 255, 255);"><p><em><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">Data transmission</span></span></em></p></td><td style="background-color: rgb(255, 255, 255);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">No data is sent before a user consents -&nbsp;not even the default consent status.</span></span></p></td><td style="background-color: rgb(255, 255, 255);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">When consent is denied, consent state and cookieless pings are sent.<br>When consent is granted, cookies are written and all measurement data is sent.</span></span></p></td></tr><tr><td style="background-color: rgb(242, 242, 242);"><p><em><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Consent states</span></span></em></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Set after user interaction.</span></span></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Defaults set to denied, unless configured otherwise;&nbsp; updates based on user choice.</span></span></p></td></tr><tr><td style="background-color: rgb(255, 255, 255);"><p><em><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">Tag behavior after user interaction</span></span></em></p></td><td style="background-color: rgb(255, 255, 255);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">Loads and executes consent mode APIs only when a user grants consent.</span></span></p></td><td style="background-color: rgb(255, 255, 255);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(255, 255, 255);">Adjusts tag behavior based on user consent choice.</span></span></p></td></tr><tr><td style="background-color: rgb(242, 242, 242);"><p><em><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Conversion modeling</span></span></em></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">General model (less detailed modeling).</span></span></p></td><td style="background-color: rgb(242, 242, 242);"><p><span style="color:rgb(31, 31, 31);"><span style="background-color:rgb(242, 242, 242);">Advertiser-specific model (more detailed modeling).</span></span></p></td></tr></tbody></table>

taken from: https://support.google.com/google-ads/answer/10000067?hl=en

<br />

## What does this mean for Google based tags (GA4, Ads, Floodlight, etc)?

<table><tbody><tr><td><p><strong>Basic Consent Mode</strong></p></td><td><p><strong>Advanced Mode</strong></p></td></tr><tr><td><p>No Google Tags will fire if set up correctly</p></td><td><p>Google Tags will fire based on trigger</p></td></tr><tr><td><p>There should be no network traffic in respect of this</p></td><td><p>Default Consent states will be set and communicated, a network request (gcs event) confirming this will be present in your network traffic, see <a href="http:#?target=JRI-GCBU-8GF-ZHS" target="_self">here</a> for more info on these</p></td></tr><tr><td><p>No Privacy based data will be collected until relevant consent is granted</p></td><td><p>No Privacy based data will be collected until relevant consent is granted</p></td></tr></tbody></table>

<br />

<div class="sd-callout" data-callout-type="alert"><strong>Disclaimer:</strong> This is a summary highlighting the key differences between the two modes and is not intended to replace Google's documentation. While all efforts are made to keep this as up to date as possible it is ultimately up to the user to make an informed decision based on their own preferences and any relevant regulatory requirements.</div>

<br />