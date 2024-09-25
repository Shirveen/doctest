---
description: "Learn how to implement Google Consent Mode V2 using Google Tag Manager (GTM) with TRUENDO. Follow step-by-step instructions to set up both Basic and Advanced Consent Modes in GTM. Last updated July 5, 2024.\n"
keywords:
    - TRUENDO
    - 'Consent Mode V2'
    - 'Google Tag Manager'
    - GTM
    - 'Data Privacy'
    - 'Website Customization'
canonical_url: 'https://docs.truendo.com/guides/google-consent-mode-v2/implementing-consent-mode-v2-with-gtm'
og_title: 'TRUENDO and Consent Mode V2 in GTM - TRUENDO Documentation'
og_description: "Discover how to set up Google Consent Mode V2 in Google Tag Manager (GTM) with TRUENDO. Implement both Basic and Advanced Consent Modes in GTM using our detailed guide.\n"
author: 'TRUENDO Team'
date_modified: '2024-07-05'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Implementing Consent Mode V2 with GTM'
id: 0B2-VIYU-VYG-YBL
slug: implementing-consent-mode-v2-with-gtm
isVisible: true
lastUpdated: '2024-07-31 09:17:44'
---
# TRUENDO and Consent Mode V2 in GTM

Welcome! If you're looking to implement Advanced or Basic Consent Mode in Google Tag Manager (GTM) using TRUENDO, you're in the right place. We'll walk you through each step to ensure you get everything set up smoothly. This guide is designed for new users, so don’t worry if you’re not familiar with the process. This guide will take you through the process of enabling Consent Mode in GTM. downloading, importing and configuring the TRUENDO tag template in GTM and setting it up. Let’s get started!

<br />

## Common steps

**Follow steps 1-6 first** then select specific instructions for [Advanced](#advanced-consent-mode) or [Basic](#advanced-consent-mode) Consent mode setup.

### Step 1: Enable Consent Mode in GTM

First, we need to enable consent mode in GTM.

1\. **Log in to your Google Tag Manager (GTM) account** and open the container you want to work with.

2\. On the top menu, click on **‘Admin’**.

3\. Under the 'Container' section, select **‘Container Settings’.<br />
**<img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/u3gDUAeOq6mkPLlWA4XF.png">

4\. In the settings, look for the **‘Additional Settings’** section.

5\. Find and tick the checkbox next to **‘Enable consent overview (BETA)’**.

6\. Click ‘**Save**’ to apply these settings.

Great! You’ve just enabled consent mode in GTM.

<br />

### Step 2: Import the TRUENDO Tag Template

Next, let’s import the template into your GTM Workspace.

1\. In GTM, navigate to the **Workspace** tab of your container.

2\. On the left menu, click on **‘Templates’**.

3\. Click the **‘Search Gallery’** button in the 'Tag Templates' panel.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/43lztzngWrY7iLiocJ5a.png"></figure>

4\. The Community Template Gallery panel will open, **click the magnifying glass** and search for TRUENDO.

<figure style="width:49%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/9KIV5SbH4Nbbk1lLwlv4.png" width="49%"></figure>

5\. Find and Click the '**TRUENDO Cookie Consent Management' by truendo-tech** template

<figure style="width:49%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/1n3rjshw7lWdLZM6bfIW.png" width="49%"></figure>

6\. Click the blue **Add to workspace** button then click **Add** on the window that will pop up. Dont be alarmed by the warning symbol, this just lets you know that the TRUENDO CMP script will be added to your website by GTM.

<br />

<figure style="width:47%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/ZhPlFzmMDvTefsD0SSUo.png" width="47%"></figure>

<figure style="width:47%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/hsWkHLnwnayp4cx28XYs.png" width="47%"></figure>

7\. The TRUENDO tag template will now appear in the tag template panel.

<figure style="width:74%"><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/WK4gSSB5KCY6P4PHv69Q.png" width="74%"></figure>

<br />

### ‍Step 3: Create a New TRUENDO Tag

### Now, let’s create a new tag using the TRUENDO template.

1\. In GTM, click on **‘Tags’** from the left menu.

2\. Click the **‘New’** button in the top right corner.

3\. A new screen will appear titled 'Untitled Tag'. Let’s give it a name—how about **‘TRUENDO’**?

4\. Click on the **'Tag Configuration’** box.

5\. Scroll down to the ‘Custom’ section and select the **TRUENDO tag** you added earlier.

6\. In the tag settings, check the boxes for **‘Inject TRUENDO via GTM’** and **‘Enable TRUENDO triggers’**.

<img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/fh65K1ufo8nIWN0W3jiW.png" width="649px">

7\. Keep this window open for the next step.

You’re doing great!

‍

### Step 4: Add Your Site ID to the TRUENDO Tag

We need to add your TRUENDO Site ID to the tag.

1\. Open a new browser tab and **log in to your TRUENDO Console**.

2\. Select your organization and website.

3\. In the left menu, click on **‘Banner’**.

4\. Scroll down to **‘Integration via script’** and click **‘Copy Site ID’**.

5\. Go back to your GTM tab and paste the Site ID in the appropriate field.

<br />

### Step 5: Configure the Consent Initialization Trigger

Next, we’ll set up the trigger that initializes consent.

1\. In your open Tag Editor, find the **‘Triggering’** section and click the **pencil icon** to edit.

2\. Choose **‘Consent Initialization - All Pages’** from the list.

3\. Click **‘Save’**.

<br />

## Advanced Consent Mode

Guess what?! By Following steps 1-6 above you have already completed the process for setting up Advanced Consent Mode and TRUENDO in GTM. **CONGRATULATIONS!!!**

<br />

### Is it working?

Click [here](http:#?target=O8B-ZNMD-DIS-QDJ) to find out how to check if your setup is working properly

<br />

## Basic Consent Mode

Please make sure you have followed steps 1-6 above before proceeding

### <br />

### Step 6: Create Custom TRUENDO Triggers

Now, we’ll create specific triggers for TRUENDO.

1\. In GTM, go to the **‘Triggers’** section from the left menu.

2\. Click the **‘New’** button in the top right corner.

3\. Name your new trigger ‘**truendo\_initialized**’ (this helps keep things organized).

4\. Click on the **‘Trigger Configuration’** box.

5\. Select **‘Custom Event’** from the list.

6\. In the event name field, type **‘truendo\_initialized’** exactly as shown.

7\. Click **‘Save’**.

You’ll need to repeat this process for several more triggers. Here are the details:

<table><tbody><tr><td><p><strong>Trigger Name</strong></p></td><td><p><strong>Event Name</strong></p></td></tr><tr><td><p>truendo_initialized</p></td><td><p>truendo_initialized</p></td></tr><tr><td><p>truendo_marketing</p></td><td><p>truendo_cc_marketing</p></td></tr><tr><td><p>truendo_preferences</p></td><td><p>truendo_cc_preferences</p></td></tr><tr><td><p>truendo_social_content</p></td><td><p>truendo_cc_social_content</p></td></tr><tr><td><p>truendo_social_sharing</p></td><td><p>truendo_cc_social_sharing</p></td></tr><tr><td><p>truendo_statistics</p></td><td><p>truendo_cc_statistics</p></td></tr></tbody></table>

### <br />

### Step 7: Configure Tags to Fire Based on Consent

### Finally, we’ll make sure tags only fire if the user has given consent.

1\. Go back to **‘Tags’** in GTM.

2\. Select the tag you want to configure for Basic Consent Mode.

3\. Click the **pencil icon** in the ‘Tag Configuration’ section.

4\. Expand the '**Advanced Settings’** and then the ‘**Consent Settings**’ sections.

5\. Check ‘**Require additional consent for tag to fire’.**

6\. Click **‘Add required consent**’ and select the necessary consent permission.

7\. Add a new trigger that matches the consent permission.

Here’s a quick reference for the triggers and their permissions:

<table><tbody><tr><td><p><strong>Trigger Name</strong></p></td><td><p><strong>Consent Permission</strong></p></td></tr><tr><td><p>truendo_marketing</p></td><td><p>ad_storage</p></td></tr><tr><td><p>truendo_marketing</p></td><td><p>ad_user_data</p></td></tr><tr><td><p>truendo_marketing</p></td><td><p>ad_personalization</p></td></tr><tr><td><p>truendo_statistics</p></td><td><p>analytics_storage</p></td></tr><tr><td><p>truendo_preferences</p></td><td><p>functionality_storage</p></td></tr><tr><td><p>truendo_preferences</p></td><td><p>personalization_storage</p></td></tr><tr><td><p>truendo_social_content</p></td><td><p>social_content</p></td></tr><tr><td><p>truendo_social_sharing</p></td><td><p>social_sharing</p></td></tr></tbody></table>

8\. Click **‘Save’**.

Great you are all set up but how do you know if everything is working as it should be ?

Click [here](http:#?target=O8B-ZNMD-DIS-QDJ) to find out

Remember if you would like to see more details on any of the above steps you can have a look at our [documentation](http:#?target=SAL-PF6J-EMH-GQE) section on TRUENDO and Google Consent Mode aswell.