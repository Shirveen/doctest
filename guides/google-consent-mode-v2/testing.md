---
description: "Learn how to test your Consent Mode setup with TRUENDO to ensure it is working as expected. Follow our guide to verify your settings using GTM Tag Assistant and network traffic monitoring. Last updated July 5, 2024.\n"
keywords:
    - TRUENDO
    - 'Consent Mode Testing'
    - 'Google Tag Manager'
    - 'GTM Tag Assistant'
    - 'Data Privacy'
    - 'Google Analytics'
canonical_url: 'https://docs.truendo.com/guides/google-consent-mode-v2/testing'
og_title: 'Testing Consent Mode - TRUENDO Documentation'
og_description: "Ensure your Consent Mode setup with TRUENDO is functioning correctly by following our detailed testing guide. Learn how to use GTM Tag Assistant and monitor network traffic.\n"
author: 'TRUENDO Team'
date_modified: '2024-07-05'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: Testing
id: O8B-ZNMD-DIS-QDJ
slug: testing
isVisible: true
lastUpdated: '2024-07-31 10:08:34'
---
# Testing

This section will help figure whether your Consent Mode setup with TRUENDO is working as it should be. We will highlight some key aspects so that you can be confident about your setup.<br />

## GTM

This section will assist you in testing your Consent Mode settings if you have configured Consent Mode via GTM

<br />

### Using The Tag Assistant

The GTM tag assistant is very useful in monitoring events, triggers, tag behavior and consent all within GTM.

1.  **Launching the Tag assistant and connecting it to a URL:** The Tag Asisstant is accesessed by clicking the **Preview** button in the top right of the GTM workspace window (next to the Submit button). Once you have configured all your tags, triggers, etc, click the preview.
    
    <figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/R9v9UrC9ArpHrebEKsiG.jpg"></figure>
    
2.  Once clicked a separate browser _page_ will open and you will be prompted to enetr a URL. This URL should correspond to a site where you have integrated the selected GTM container. This can be a live site or test site just remember to make sure that you have integrated the correct container. Once you enter the URL click **Connect**.
    
    <figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/HAAaVBzDGGwvoRZk4GMk.jpg"></figure>
    
3.  Once you enter the URL click connect and a separate browser _window_ will open the URL you specified. **Do not click anything and we mean anything** in this browser window yet as tempting as it may be DO NOT click Finish or anything on the TRUENDO banner that will have popped up if you have any privacy relevant services running on this page such as Google Analytics or Google Ads.
4.  Click into the previous browser window into the Tag Assistant page (for ease of reference we will call this **Window A** going forward), you should see a pop up that says Connected. Click the blue Continue button. You should be met with a screen that resembles the following
    
    <figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/zHinXS0qqMDU6xmsJA84.png"></figure>
    
    <br />
    
5.  In the screen shot above the left panel, titled Summary shows on page events that have occured while the main window displays the status of tags amongst other things. You will note in the example the TRUENDO tag has fired without consent. The TRUENDO tag should always fire regardless of consent if configured properly as it is what is requesting the consent. For now we will ignore the fact that the Analytics tag has fired, we will come back to this in the Advanced Consent mode section that follows.
6.  Under the **Summary** panel click the **Consent Default** event, then in the main window click the consent tab. If configured correctly yours should look very similar to this:
    
    <img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/KK85ImPxV10HHzMzlhQR.png">
    
    <br />
    
7.  Now back in the test browser window that loaded your URL, make a consent decision on the TRUENDO banner. For the purposes of this guide we have clicked 'Accept All'. Now look back at **Window A**
8.  You will see under the **Summary** panel a **'Consent Update'** event has occured. Click it and again click the consent tab if the main window is not already on it. Your screen should look alot like this one:<img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/Ljllz5daKNKUjqjF8Rai.png">
    
    <br />
    
9.  If the consent has updated then Congrats all looks in order and you are good to go. If you clicked Necessary Only or customized your consent choices then the respective categories should be Granted or Denied accordingly. You can perform additional checks using network traffic monitoring in the browser see the section below. check the following two secions for what to look out for in **Advanced** and **Basic** consent mode.<br />
    You will notice two categories in our example are still denied, this is simply because we do not have any relevant tags or triggers in these categories in this container.
    
    <br />
    

#### <br />

#### Advanced Consent Mode

Rememebr in this mode regardless of consent Google tags are supposed to fire based on trigger but will not communicate any privacy relevant data.

The above screen shot in Step 1.4 shows just this where the Google Analytics tag has fired before consent has been granted.

<br />

#### Basic Consent Mode

In this instance no Google Tags should have fired before consent . So the above screen shot will show that the Google analytics Tag has not been fired but will be after consent is granted ie after the Consent Update.

<br />

### By Looking at Network Traffic

If you have not used GTM to initialize Consent Mode or simply want to verify that all is working as it should outside of the Tag Assistant then read on.

<br />

1.  You will to visit the site you are testing in a clean browsing environments, this means a cleared cache. The simplest way of doing continual testing is to use a Private/Incognito window when visiting the site. Do not click anything once the site loads ie do not interact with the TRUENDO banner
2.  RIght click on the page and then Click on 'Inspect', the browser's Developer tools screen will appear in a new window. Now click the Network tab.
3.  Reload the web page in its window (again without accepting or clicking anything else) or you can usually use the keyboard shortcut F5 to reload the page from the Developer Tools screen (this may differ based on Browser or Keyboard).

<br />

In **Advanced consent mode** you will see a **_'collect'_** request before consent is granted for any relevant service such as Google Analytics. if you click on this request you will then be able to view its request url, in there you will see a **_gcs_** parameter

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/bUZvNbmFlsv7Oj3Mj4xn.png"></figure>

<br />

<img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/ul0XQPou0ifTmKNCbj8z.png">

<br />

The value of this parameter should be either 100 or 000 before consent or when consent is denied but will change if granted.

See below for a summary of these gcs values.

<span style="color:rgba(10,10,10,1);">- </span> `gcs=G100`: Both analytics\_storage and ad\_storage are denied.

<span style="color:rgba(10,10,10,1);">- </span> `gcs=G110`: Analytics\_storage is denied, ad\_storage is granted.

<span style="color:rgba(10,10,10,1);">- </span> `gcs=G101`: Analytics\_storage is granted, ad\_storage is denied.

<span style="color:rgba(10,10,10,1);">- </span> `gcs=G111`: Both analytics\_storage and ad\_storage are granted.

<span style="color:rgba(10,10,10,1);">- </span> `gcs=G1--`: Consent for ad\_storage or analytics\_storage was not required by the site

<br />

In **Basic consent mode** before consent you should simply **not see any collect request** but after a consent has been granted the above should be present.

<br />

<br />

<br />

<br />