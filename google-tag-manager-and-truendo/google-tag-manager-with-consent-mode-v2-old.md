---
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Google Tag Manager with Consent Mode V2 old'
id: WW7-JHQZ-PM3-O2N
slug: google-tag-manager-with-consent-mode-v2-old
isVisible: true
lastUpdated: '2024-08-08 13:06:50'
---
# Google Tag Manager With Consent Mode V2 Enabled (Without using the TRUENDO tag template)

<div class="sd-callout" data-callout-type="tip"><p>Please note this part of the documentation if for reference only and for users who implemented TRUENDO in GTM before the introduction of the TRUENDO Tag Template in GTM. <strong>This is no longer the recommended method for implementing TRUENDO in GTM.</strong></p></div>

<div class="sd-callout" data-callout-type="alert"><p>Before proceeding please <strong>remove/deactivate any existing scripts/plugins you may have previously used to integrate TRUENDO</strong> on your website. Google Tag manager will do it automatically once the procedure below is completed.</p></div>

<div class="sd-callout" data-callout-type="info"><p>Please ensure that the TRUENDO Tag fires <strong>before</strong> all other privacy relevant tags</p></div>

### <span style="color:rgb(0, 0, 0);">Step 1</span>

<span style="color:rgb(14, 16, 26);">Enable Google's Consent Mode by navigating to the Admin tab in Google Tag Manager, selecting the Container Settings option, and ticking the </span> **<span style="color:rgb(14, 16, 26);">Enable consent overview (BETA)</span>** <span style="color:rgb(14, 16, 26);">checkbox under Additional Settings, click </span> **<span style="color:rgb(14, 16, 26);">Save</span>**<span style="color:rgb(14, 16, 26);">.</span>

<br />

### Step 2

Paste the following code snippet ahead of the GTM script . This script must be present on every page where GTM is present, This is a prerequisite stipulated by Google. We recommend you integrate it the same way you integrate GTM.

```
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag() {
      dataLayer.push(arguments);
    }

    // set „denied' as default for both ad and analytics storage,
    gtag("consent", "default", {
      ad_storage: "denied",
      ad_user_data: "denied",
      ad_personalization: "denied",
      analytics_storage: "denied",
      preferences: "denied",
      social_content: "denied",
      social_sharing: "denied",
      wait_for_update: 500, // milliseconds to wait for update
    });

    // Enable ads data redaction by default [optional]
    gtag("set", "ads_data_redaction", true);
</script>
```

### <span style="color:rgb(0, 0, 0);">Step 3</span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Download our Tag Manager JSON file for Consent Mode. This contains the necessary tag and variables without the triggers.</span></span>

[<span style="color:rgb(0, 85, 187);"><span style="background-color:transparent;">Download TRUENDO-GTM-CONSENT-MODE JSON</span></span>](https://truendo-file-hosting.s3.eu-central-1.amazonaws.com/TRUENDO-GTM-CONSENT-MODE.json)

### Step 4

Import the above file to Google Tag Manager as a container:

1.  Go to the **Admin Tab** and click on **Import Container** option.
2.  Upload the **TRUENDO-GTM-CONSENT-MODE.json** file by clicking **Choose container file**.
3.  Click **Existing** and set the workspace to Default Workspace.
4.  Set the import options to **Merge**. Click **Confirm.**<img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/eBAEIoNsq6MSynpdJFpB.png">

<div class="sd-callout" data-callout-type="alert"><p><strong><span style="color:rgb(0, 0, 0);">Important:</span></strong><span style="color:rgb(0, 0, 0);"> Be sure to only merge and not overwrite when importing. Otherwise you might lose your existing tags within Google Tag Manager.</span></p></div>

<div class="sd-callout" data-callout-type="info"><p><strong>Important Note:</strong> This JSON file is different from the file provided to integrate Google Tag Manager without Consent Mode. If you have previously imported the TRUENDO tag: when selecting the <strong>Merge</strong> option, choose the sub-option <strong>Overwrite conflicting tags, triggers and variables</strong>. Be sure to also remove any TRUENDO triggers from other tags (<em>truendo_statistics, truendo_marketing</em>) as it will prevent Consent mode from working.</p></div>

### Step 5

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Now you need to add your Site ID to the TRUENDO tag.</span></span>

1.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Log in to the TRUENDO </span></span> [<span style="color:rgb(0, 85, 187);"><span style="background-color:transparent;">Console</span></span>](https://console.truendo.com/), (select the correct Organization and website if you have more than one) then click **Banner** in the panel on the left of the screen, now scroll until you see **Integration via script**.
2.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Click </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Copy Site ID</span></span>**<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>
3.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Back in Google Tag Manager under the Tags tab, open the </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">TRUENDO</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">tag.</span></span>
4.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Now replace </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">YOUR WEBSITE ID</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">text (found near the bottom of the code block) with the ID you copied from the console, simply highlight and paste. Do not delete/replace the quotation marks.</span></span>
5.  Click **Save** and close the tag.

### <span style="color:rgb(0, 0, 0);">Step 6</span>

Your tags will require additional consent settings if there is no preset consent setting for it<span style="color:rgb(0, 0, 0);">.</span>

<div class="sd-callout" data-callout-type="alert"><p>By default <strong>Google tags</strong> such as <strong>Google Analytics</strong> and <strong>Google Ads</strong> come with built in consent configurations, See below <strong>Google Tags</strong></p></div>

For any other tags that require consent configuration you can additional consent for each tag according to your requirements the following consent tags are available:

-   `ad_storage`
-   `analytics_storage`
-   `ad_user_data`
-   `ad_personalization`
-   `preferences`
-   `social_content`
-   `social_sharing`
    
    <br />
    
    <span style="color:rgb(0, 0, 0);">To do this click on the tag to be modified to open the </span> **<span style="color:rgb(0, 0, 0);">Tag Configuration</span>** <span style="color:rgb(0, 0, 0);">menu. Expand the </span> **<span style="color:rgb(0, 0, 0);">Advanced Settings</span>** <span style="color:rgb(0, 0, 0);">dropdown and then expand the </span> **<span style="color:rgb(0, 0, 0);">Consent Settings</span>** <span style="color:rgb(0, 0, 0);">dropdown check the </span> **<span style="color:rgb(0, 0, 0);">Require additional consent for tag to fire </span>** <span style="color:rgb(0, 0, 0);">option</span> <span style="color:rgb(0, 0, 0);">and type in the corresponding category:</span>
    

<br />

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/mVDn4RnnA5rJUYTyGvfY.png"></figure>

<span style="color:rgb(0, 0, 0);">Click </span>[<span style="color:rgba(59,103,251,1);">here </span>](https://developers.google.com/tag-platform/devguides/consent)<span style="color:rgb(0, 0, 0);">to access more information on Google Consent Mode</span>.

<br />

## Triggers and tag order

It is vital that tags requiring consent are only fired once all consent settings have been loaded, to make this as easy as possible TRUENDO provides a trigger called `truendo_initialized`_._ Tags that previously fired on the "page view" trigger for example would now use `truendo_initialized` as the trigger to ensure consent before the specific tag fires.

<br />

<br />