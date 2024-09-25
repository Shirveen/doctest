---
description: "Learn how to configure language settings for TRUENDO’s Cookie Manager, available in 32 different languages. Customize main and supported languages to match your audience. Last updated June 19, 2024.\n"
keywords:
    - TRUENDO
    - 'Language Settings'
    - 'Cookie Manager'
    - 'Multilingual Support'
    - 'Data Privacy'
    - 'Website Customization'
canonical_url: 'https://docs.truendo.com/language-settings'
og_title: 'Language Settings - TRUENDO Documentation'
og_description: "Follow our guide to configure language settings for TRUENDO’s Cookie Manager. Choose from 32 different languages and customize main and supported languages for your website.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-19'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Language Settings (Duplicate)'
id: 65A-SVJU-5V3-9B3
slug: language-settings-duplicate
isVisible: true
lastUpdated: '2024-09-23 12:14:58'
---
# <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Language Settings</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">TRUENDO’s Cookie Manager is now available in 32 different Languages.</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">These are Albanian, Arabic, Bosnian, Bulgarian, Chinese(simplified), Chinese (traditional), Czech, Croatian, Danish, Dutch, English, Estonian, Finnish, French, German, Greek, Hungarian, Italian, Latvian, Lithuanian, Norwegian, Polish, Portuguese, Portuguese (Brazilian), Romanian, Russian, Serbian, Slovak, Slovenian, Spanish, Swedish and Turkish.</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Depending on your package your can choose one or more languages from your Console settings.</span></span>

<iframe src="https://www.youtube.com/embed/M9WDU5XjI7s?showinfo=0" frameborder="0" allowfullscreen="true" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" width="100%"></iframe>

<br />

## Basic Configuration

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 1</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">In the Console go to </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Banner</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">in the left menu panel. Scroll down to </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Active languages</span></span>**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>

<img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/w0JgJaMCVflzzQW5aMEj.png" alt="">

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 2</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Click the dropdown arrow under </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Main Language</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">and set the language users see if they use a browser language outside of our supported languages. Click </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Supported Languages</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">and select all the languages you want your Cookie Manager to be displayed in.</span></span>

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 3</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Click </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Save</span></span>**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>

---

<br />

## Language Override

By default TRUENDO sets the language of the banner as the main language or one of the supported languages based on the language of the website visitor's browser. This override may be useful in cases where a website has some form of language picker. TRUENDO allows website administrators to programmatically set TRUENDO's language. This cannot be done directly from the TRUENDO console but by the **addition of an attribute** to the TRUENDO [integration script](http:#?target=6FY-XTZ-IMX-OWH).

<br />

<div class="sd-callout" data-callout-type="info"><p>TRUENDO must first be integrated successfully to a website in order to implement the language override</p></div>

### Step 1

The language you wish to use must first be added to the Supported Languages of the website.

### Step 2

Add the attribute `data-lang='language-code'` to the end of the TRUENDO script, either by using javascript or on the server side with the relevant technology. Where language code is replaced with the code of the specific language you wish to use. A full list of supported language codes may be found below.

<br />

It should look something like this:

```
<script
id="truendoAutoBlock"
type="text/javascript"
src="https://cdn.priv.center/pc/truendo_cmp.pid.js"
data-siteid="siteID"
data-lang="language-code"
></script>
```

<div class="sd-callout" data-callout-type="info"><p>Note that on your website the <code>"siteID"</code> will already contain your specific website ID provided TRUENDO has been integrated.</p></div>

Language code table

<table><tbody><tr><th><p>French</p><p>Italian</p><p>Bulgarian</p><p>Croatian</p><p>Czech</p><p>Danish</p><p>Dutch</p><p>Estonian</p><p>Finnish</p><p>Greek</p><p>Hungarian</p><p>Lithuanian</p><p>Norwegian</p><p>Portuguese</p><p>Romanian</p><p>Russian</p><p>Slovak</p><p>Slovenian</p><p>Spanish</p><p>Swedish</p><p>Latvian</p><p>Polish</p><p>Turkish</p><p>Albanian</p><p>Bosnian</p><p>Serbian</p><p>Arabic</p><p>Chinese (Simplified)</p><p>Chinese (Traditional)</p><p>English</p><p>German</p><p>Portuguese (Brazilian)</p></th><th><p>fr</p><p>it</p><p>bg</p><p>hr</p><p>cs</p><p>da</p><p>nl</p><p>et</p><p>fi</p><p>el</p><p>hu</p><p>lt</p><p>no</p><p>pt</p><p>ro</p><p>ru</p><p>sk</p><p>sl</p><p>es</p><p>sv</p><p>lv</p><p>pl</p><p>tr</p><p>sq</p><p>bs</p><p>sr</p><p>ar</p><p>cn</p><p>hk</p><p>en</p><p>de</p><p>pt-br</p></th></tr></tbody></table>

<br />

## <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">FAQs</span></span>

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">How does TRUENDO know which language to display the Cookie Manager/Consent Banner in?</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">There is an order in which TRUENDO selects which language to be displayed in. See below:</span></span>

**Summary of Display Language Priority in Descending Order**

<table><tbody><tr><td><p>Language Override</p></td><td><p>This is an attribute added to the TRUENDO Script , <strong>it is not present in the TRUENDO script by default and must be added by a site admin </strong>see above. If this language is not a main/supported language then TRUENDO will display in the Main language by default</p></td><td><p><br></p></td></tr><tr><td><p>HTML meta data</p></td><td><p>This is a language descriptor in the code of the website itself . If this language is not a main/supported language then TRUENDO will display in the Main language by default</p></td><td><p><br></p></td></tr><tr><td><p>Website Visitor Browser Language</p></td><td><p>TRUENDO will display in the language of a website visitor's browser provided that the language is one selected as a Main or Supported language in TRUENDO, if the visitor browser language is not a Main/Supported language then TRUENDO will display in the Main language which is ENGLISH by default but can be changed.</p></td><td><p><br></p></td></tr></tbody></table>

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">What is the difference between a Main Language and a Supported Language?</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">The </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Main Language</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">is the fallback language. That means, if a user visits your website and the Cookie Manager is not available in their browser’s language or that selected by any other means as described above, the display language will fallback to the </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Main Language</span></span>**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>

<br />

<table><tbody><tr><td><p><br></p></td><td><p><br></p></td></tr></tbody></table>

<br />