---
description: "Learn how to set up Advanced Consent Mode in Google Tag Manager (GTM) with our step-by-step guide.  Enable Google's Consent Mode, download and import the TRUENDO Tag Template, and configure consent  states for optimal data privacy management. Last updated June 19, 2024.\n"
keywords:
    - TRUENDO
    - 'Advanced Consent Mode'
    - 'Google Tag Manager'
    - GTM
    - 'Consent Management'
    - 'Data Privacy'
    - 'GDPR Compliance'
canonical_url: 'https://docs.truendo.com/advanced-consent-mode-in-gtm'
og_title: 'Advanced Consent Mode in GTM - TRUENDO Documentation'
og_description: "Follow our detailed guide to set up Advanced Consent Mode in Google Tag Manager (GTM).  Enable Google's Consent Mode, configure consent states, and ensure GDPR compliance.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-19'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Advanced Consent Mode in GTM'
id: RRK-AEO3-EIM-GWV
slug: advanced-consent-mode-google-default
isVisible: true
lastUpdated: '2024-07-31 09:19:19'
---
# Advanced Consent Mode in GTM<br />

Advanced Consent Mode is the standard manner in which GTM is set up with consent mode active. In this mode Google tags load when a user opens the website or app.<br />
<br />
The tags load the consent mode API and do the following:

-   Set **default consent states**. By default, consent will be denied, unless you set your own defaults.

<div class="sd-callout" data-callout-type="alert"><strong>While consent is denied, the Google tags send cookieless pings.</strong></div>

Wait for user interaction with the banner and update consent states.

Only when a user **grants consent to data collection, Google tags send the full measurement data.**

<br />

TRUENDO now offers a GTM Tag Template to make setting up TRUENDO in GTM easier than ever

<div class="sd-callout" data-callout-type="alert">Before proceeding please <strong>remove/deactivate any existing scripts/plugins you may have previously used to integrate TRUENDO</strong> on your website. Google Tag manager will do it automatically once the procedure below is completed.</div>

### <span style="color:rgb(0, 0, 0);">Step 1</span>

<span style="color:rgb(14, 16, 26);">In Google Tag manager (GTM) enable Google's Consent Mode by navigating to the 'Admin' tab, selecting the 'Container Settings' option, and ticking the </span> **<span style="color:rgb(14, 16, 26);">Enable consent overview (BETA)</span>** <span style="color:rgb(14, 16, 26);">checkbox under 'Additional Settings', click </span> **<span style="color:rgb(14, 16, 26);">Save</span>**<span style="color:rgb(14, 16, 26);">.</span>

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/u3gDUAeOq6mkPLlWA4XF.png"></figure>

### Step 2

Import the TRUENDO Tag Template for GTM to your workspace by clicking 'Templates' from the panel on the left and then Search Gallery in the Tag Templates panel.<img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/43lztzngWrY7iLiocJ5a.png" width="947px">_<br />
<br />
<br />
_Step 3

Click the Magnifying glass in the panel that appears and search for TRUENDO and click the **TRUENDO Cookie Consent Management by truendo-tech** template

<figure style="width:51%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/1n3rjshw7lWdLZM6bfIW.png" width="51%"></figure>

### Step 4

Click the blue 'Add to workspace' and confirm addition of the template in the window that pops up. The TRUENDO Tag template will appear in the Tag Templates panel once done.

<figure style="width:64%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/ZhPlFzmMDvTefsD0SSUo.png" width="64%"></figure>

<figure style="width:62%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/hsWkHLnwnayp4cx28XYs.png" width="62%"></figure>

<figure style="width:65%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/WK4gSSB5KCY6P4PHv69Q.png" width="65%"></figure>

<br />

### Step 5

Click 'Tags' in the panel on the left. Then click the 'New' button in the top right of the 'Tags' screen.

<img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/qVnqzgXBNuQ883mug005.png">

<br />

### Step 6

An 'Untitled Tag' screen will appear containing the 'Tag Configuration' and 'Triggering' panes. Rename this tag to TRUENDO, this is not necessary but recommended to help you keep track.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/hHSVTL3zbSagKwgy4J1Y.png"></figure>

### Step 7

Click the Edit (pencil) button that appears when you hover in the top right of the 'Tag Configuration' pane. Scroll down to Custom and select the TRUENDO tag you just added.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/pXfcO7UcGnFmZDHKNH42.png"></figure>

### Step 8

Tick the checkbox titled 'Inject TRUENDO via GTM'. Check any additional check boxes based on your preferences. Leave the Tag editor pane open and proceed to the next step. Do not close or save this yet.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/0ZeJhBTgSGeW513ePu0c.png"></figure>

### Step 9

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Now you need to add your Site ID to the TRUENDO tag. In a separate browser window to GTM:</span></span>

1.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Log in to the TRUENDO </span></span> [<span style="color:rgb(0, 85, 187);"><span style="background-color:transparent;">Console</span></span>](https://console.truendo.com/), (select the correct Organization and website if you have more than one) then click **Banner** in the panel on the left of the screen, now scroll until you see **Integration via script**.
2.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Click </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Copy Site ID</span></span>**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>
3.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Back in Google Tag Manager in the already opened Tag Editor paste the Site ID in the field provided</span></span>

### Step 10

Click the Edit button in the Triggering pane, then select 'Consent Initialization - All Pages' in the screen that appears.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/PuNnCAmBIF5Yt4e1SMzL.png"></figure>

### Step 11

Click **Save**, Congratulations you have succesfully setup TRUENDO in Google Tag Manager.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/8lhPkX3Z8GNXrasuZg6x.png"></figure>

<br />