---
description: "Learn how to implement Basic Consent Mode in Google Tag Manager (GTM) with our step-by-step guide.  Prevent Google tags from loading until user consent is obtained, ensuring no data is transferred without consent.  Last updated June 19, 2024.\n"
keywords:
    - TRUENDO
    - 'Basic Consent Mode'
    - 'Google Tag Manager'
    - GTM
    - 'Consent Management'
    - 'Data Privacy'
    - 'GDPR Compliance'
canonical_url: 'https://docs.truendo.com/basic-consent-mode-in-gtm'
og_title: 'Basic Consent Mode in GTM - TRUENDO Documentation'
og_description: "Follow our detailed guide to implement Basic Consent Mode in Google Tag Manager (GTM).  Prevent Google tags from loading until user consent is obtained, ensuring GDPR compliance.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-19'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Basic Consent Mode in GTM'
id: DJP-RRA8-Q55-TVJ
slug: basic-consent-mode-in-gtm
isVisible: true
lastUpdated: '2024-07-31 12:12:06'
---
# Basic Consent Mode in GTM<br />

<div class="sd-callout" data-callout-type="info"><strong>By default, all Google tags operate in advanced consent mode.</strong><br><br>In order to change this, you will need to <strong>configure the tag to only fire if consent has been obtained</strong>.</div>

<span style="color:#1F1F1F;">When you implement consent mode in its basic version, you prevent Google tags from loading until a user interacts with a consent banner. This setup transmits no data to Google prior to user interaction with the consent banner.</span>

**<span style="color:#1F1F1F;">If the user does not consent, no data is transferred to Google at all</span>** <span style="color:#1F1F1F;">– not even the consent status. Google tags are completely blocked from firing</span>

<br />

## **<span style="color:#1F1F1F;">Implementing Basic Consent Mode</span>**

#### Step 1

In Google Tag manager (GTM) enable Google's Consent Mode by navigating to the 'Admin' tab, selecting the 'Container Settings' option, and ticking the Enable consent overview (BETA) checkbox under 'Additional Settings', click Save.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/EWPdDm0Gu0RXJFAOCOQz.png"></figure>

<br />

#### Step 2

Import the TRUENDO Tag Template for GTM to your workspace by clicking 'Templates' from the panel on the left and then Search Gallery in the Tag Templates panel.<img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/43lztzngWrY7iLiocJ5a.png" width="947px">_<br />
<br />
<br />
_Step 3

Click the Magnifying glass in the panel that appears and search for TRUENDO and click the **TRUENDO Cookie Consent Management by truendo-tech** template

<figure style="width:51%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/1n3rjshw7lWdLZM6bfIW.png" width="51%"></figure>

#### Step 4

Click the blue 'Add to workspace' and confirm addition of the template in the window that pops up. The TRUENDO Tag template will appear in the Tag Templates panel once done.

<figure style="width:64%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/ZhPlFzmMDvTefsD0SSUo.png" width="64%"></figure>

<figure style="width:62%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/hsWkHLnwnayp4cx28XYs.png" width="62%"></figure>

<figure style="width:65%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/WK4gSSB5KCY6P4PHv69Q.png" width="65%"></figure>

#### Step 5

Click 'Tags' in the panel on the left. Then click the 'New' button in the top right of the 'Tags' screen.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/myjJ8iBgf1ycatvpIWqj.png"></figure>

<br />

#### Step 6

An 'Untitled Tag' screen will appear containing the 'Tag Configuration' and 'Triggering' panes. Rename this tag to TRUENDO, this is not necessary but recommended to help you keep track.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/2NbNZHb63Fw5bD9yXREL.png"></figure>

<br />

#### Step 7

Click the Edit (pencil) button that appears when you hover in the top right of the 'Tag Configuration' pane. Scroll down to Custom and select the TRUENDO tag you just added.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/HlWmUs2kfJAwCsiM6caq.png"></figure>

<br />

#### Step 8

Tick the checkbox titled 'Inject TRUENDO via GTM' and Tick the checkbox titled 'Enable TRUENDO triggers’. Check any additional check boxes based on your preferences. Leave the Tag editor pane open and proceed to the next step. Do not close or save this yet.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/fh65K1ufo8nIWN0W3jiW.png"></figure>

#### Step 9

Now you need to add your Site ID to the TRUENDO tag. In a separate browser window to GTM:

1.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Log in to the TRUENDO </span></span> [<span style="color:rgb(0, 85, 187);"><span style="background-color:transparent;">Console</span></span>](https://console.truendo.com/), (select the correct Organization and website if you have more than one) then click **Banner** in the panel on the left of the screen, now scroll until you see **Integration via script**.
2.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Click </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Copy Site ID</span></span>**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>
3.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Back in Google Tag Manager in the already opened Tag Editor paste the Site ID in the field provided</span></span>

#### Step 10

Click the Edit button in the Triggering pane, then select 'Consent Initialization - All Pages' in the screen that appears. Click save after this.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/dMKVV1M5eR3DhajgQZNn.png"></figure>

<br />

#### Step 11

Click 'Triggers' in the panel on the left. Then click the 'New' button in the top right of the 'Triggers' screen.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/uIS2j4rhFSyL7w3QZ1fE.png"></figure>

<br />

#### Step 12

An 'Untitled Trigger’ screen will appear containing the 'Trigger Configuration' pane. Rename this trigger to ‘truendo\_initialized’, this is not necessary but recommended to help you keep track.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/1xbYYVFDcWwlVHc3DF0h.png"></figure>

<br />

#### Step 13

Click the Edit (pencil) button that appears when you hover in the top right of the 'Trigger Configuration' pane. Scroll down and select Custom Event.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/sPKyqlDxR3BuNlf3KujX.png"></figure>

<br />

#### Step 14

Enter “truendo\_initialized” into the event field name. It is important that you type this out exactly as shown above. Leave all other settings as default. Click save after this.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/RCfVD20MuUZgBj2OKkl7.png"></figure>

#### Step 15

**Repeat Steps 12 – 15** with the following values until all triggers have been created:

<table><tbody><tr><td><p><strong>Trigger Name</strong></p></td><td><p><strong>Event Name</strong></p></td></tr><tr><td><p>truendo_initialized</p></td><td><p>truendo_initialized</p></td></tr><tr><td><p>truendo_marketing</p></td><td><p>truendo_cc_marketing</p></td></tr><tr><td><p>truendo_preferences</p></td><td><p>truendo_cc_preferences</p></td></tr><tr><td><p>truendo_social_content</p></td><td><p>truendo_cc_social_content</p></td></tr><tr><td><p>truendo_social_sharing</p></td><td><p>truendo_cc_social_sharing</p></td></tr><tr><td><p>truendo_statistics</p></td><td><p>truendo_cc_statistics</p></td></tr></tbody></table>

These triggers allow TRUENDO to control (fire) tags based on their consent setting in TRUENDO such that in the future should consent have previously been requested and granted TRUENDO will fire the respective tags.

<br />

## Configuring tags to work in Basic Consent Mode

**By default, all Google tags operate in advanced consent mode**. In order to change this, you will need to configure the tag to only fire if consent has been obtained.

<br />

#### Step 1

Click 'Tags' in the panel on the left and then click on the Tag that you wish to configure for Basic Consent Mode.

<br />

#### Step 2

Click the Edit (pencil) button that appears when you hover in the top right of the 'Tag Configuration' pane.

<br />

#### Step 3

Click the Edit button in the Triggering pane, then click on “+” icon to add a new trigger. the following screen will appear.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/6MQ7n87PmSa3V44CWidL.png"></figure>

#### Step 4

Select the custom TRUENDO trigger that corresponds to the Consent Permission that you set for the tag in **Step 5**.

<table><tbody><tr><td><p><br></p></td><td><p><strong>Trigger Name</strong></p></td><td><p><strong>Consent Permission</strong></p></td></tr><tr><td><p><br></p></td><td><p>truendo_marketing</p></td><td><p>ad_storage</p></td></tr><tr><td><p><br></p></td><td><p>truendo_marketing</p></td><td><p>ad_user_data</p></td></tr><tr><td><p><br></p></td><td><p>truendo_marketing</p></td><td><p>ad_personalization</p></td></tr><tr><td><p><br></p></td><td><p>truendo_statistics</p></td><td><p>analytics_storage</p></td></tr><tr><td><p><br></p></td><td><p>truendo_preferences</p></td><td><p>functionality_storage</p></td></tr><tr><td><p><br></p></td><td><p>truendo_preferences</p></td><td><p>personalization_storage</p></td></tr><tr><td><p><br></p></td><td><p>truendo_social_content</p></td><td><p>social_content</p></td></tr><tr><td><p><br></p></td><td><p>truendo_social_sharing</p></td><td><p>social_sharing</p></td></tr></tbody></table>

<br />

#### Step 5

Click Save, Congratulations you have successfully setup your tag for Basic Consent Mode.

<br />

<br />

### Optional: Configuring Tags without built in consent checks to work with Basic Consent Mode

<div class="sd-callout" data-callout-type="alert">This process is for adding addtional consent checks to Tags, it is <strong>not necessary for normal users</strong> but included for those that may require it.</div>

#### These steps require execution between Step 2 and Step 3<br />
<br />
Step A

#### Expand the “Advanced Settings” tab and scroll down and then expand the “Consent Settings” tab.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/MnT5HuCj8He8r5OwgKno.png"></figure>

<br />

#### Step B

Expand the "Consent Settings" section and select “Require additional consent for tag to fire”.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/yV6SfBYF0eVU4yiQuvHM.png"></figure>

<br />

#### Step C

Click the “Add required consent” button and then select the consent permission that is required for the tag to trigger.<br />
The following consent permissions are available:

-   `ad_storage`
-   `analytics_storage`
-   `ad_user_data`
-   `ad_personalization`
-   `preferences`
-   `social_content`
-   `social_sharing`

<br />

<br />