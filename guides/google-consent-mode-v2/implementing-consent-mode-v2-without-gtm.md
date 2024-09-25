---
description: "Learn how to implement Google Consent Mode without using Google Tag Manager (GTM) with TRUENDO. Follow step-by-step instructions to set up both Basic and Advanced Consent Modes by editing your website's HTML. Last updated July 5, 2024.\n"
keywords:
    - TRUENDO
    - 'Consent Mode'
    - 'Google Analytics'
    - 'Data Privacy'
    - 'HTML Integration'
    - 'Website Customization'
canonical_url: 'https://docs.truendo.com/guides/google-consent-mode-v2/implementing-consent-mode-v2-without-gtm'
og_title: 'Consent Mode not Using GTM - TRUENDO Documentation'
og_description: "Discover how to set up Google Consent Mode without using Google Tag Manager (GTM). Implement both Basic and Advanced Consent Modes directly in your website's HTML with TRUENDO.\n"
author: 'TRUENDO Team'
date_modified: '2024-07-05'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Implementing Consent Mode V2 without GTM'
id: VYR-Y9QX-5VO-ULK
slug: implementing-consent-mode-v2-without-gtm
isVisible: true
lastUpdated: '2024-07-31 09:22:56'
---
# Consent Mode not Using GTM

This guide will walk you through the process of implementing both Basic and Advanced Consent Mode outside of GTM. This will involve editting you websites HTML, don't be daunted we will make this as simple as we can showing you exactly what to add and where to add it.

<div class="sd-callout" data-callout-type="alert">This process is explicitly for when you are <strong>not using GTM to integrate Google Analytics and ONLY have Google Analytics as a Google service</strong> on your website. If you are using GTM to integrate Google Analytics click <a href="http:#?target=0B2-VIYU-VYG-YBL" target="_self">here</a> to see the appropriate step by step guide.</div>

## Common Steps

**Step 1: Insert Initial Script**

1.  **Locate the** `&lt;head&gt;` section of your website's HTML.
2.  **Insert the following script** as the very first script in the `&lt;head&gt;` section. This ensures it runs before any other scripts, including Google Analytics and other TRUENDO scripts.
    
    ```
    &lt;script&gt;
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
            &lt;/script&gt;
    ```
    

**Step 2: Implement TRUENDO Cookie Control Callback**

1.  **Add the TRUENDO Cookie Control Callback function** right after the initial script:
    
    ```
    &lt;script&gt;
              function TruendoCookieControlCallback(cookieObj) {
                if (cookieObj.preferences) {
                  gtag("consent", "update", {
                    preferences: "granted",
                  });
                } else {
                  gtag("consent", "update", {
                    preferences: "denied",
                  });
                }
                if (cookieObj.marketing) {
                  gtag("consent", "update", {
                    ad_storage: "granted",
                    ad_personalization: "granted",
                    ad_user_data:"granted",
                  });
                } else {
                  gtag("consent", "update", {
                    ad_storage: "denied",
                    ad_personalization: "denied",
                    ad_user_data:"denied",
                  });
                }
                if (cookieObj.statistics) {
                  gtag("consent", "update", {
                    analytics_storage: "granted",
                  });
                } else {
                  gtag("consent", "update", {
                    analytics_storage: "denied",
                  });
                }
                if (cookieObj.social_content) {
                  gtag("consent", "update", {
                    social_content: "granted",
                  });
                } else {
                  gtag("consent", "update", {
                    social_content: "denied",
                  });
                }
                if (cookieObj.social_sharing) {
                  gtag("consent", "update", {
                    social_sharing: "granted",
                  });
                } else {
                  gtag("consent", "update", {
                    social_sharing: "denied",
                  });
                }
              }
              &lt;/script&gt;
    ```
    

**Step 3: Create or Log in to TRUENDO Account**

**Create a TRUENDO account** or log in to your existing account at [TRUENDO Console](https://console.truendo.com/).

**Step 4: Retrieve TRUENDO Integration Script**

1.  In the TRUENDO Console, navigate to **Banner** on the left sidebar.
    
    <figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/5Bvel4mCemrDNkWOgzbQ.png"></figure>
    
2.  Scroll down to **Integration via Script** and **copy your TRUENDO snippet**, which will look something like this:
    
    ```
       &lt;!-- TRUENDO Privacy Center --&gt;
            &lt;script id="truendoAutoBlock" type="text/javascript" src="https://cdn.priv.center/pc/truendo_cmp.pid.js" data-siteid="YOUR SITE ID"&gt;&lt;/script&gt;
            &lt;!-- End TRUENDO Privacy Center --&gt;
    ```
    

**Step 5: Add TRUENDO Integration Script**

**Paste the TRUENDO snippet** in the `&lt;head&gt;` section of your website, immediately after the scripts from Step 1 and Step 2.

<br />

**Step 6: Add Google Analytics Script**

**Copy the Google Analytics script** and paste it in the `&lt;head&gt;` section immediately after the scripts from Step 1, Step 2, and Step 4. Here is an example:

```
   <!-- Google tag (gtag.js) -->
        <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXX"></script>
        <script>
          window.dataLayer = window.dataLayer || [];
          function gtag() { dataLayer.push(arguments); }
          gtag('js', new Date());

          gtag('config', 'G-xxxxxxxx');
        </script>
```

**Final Step: Save Your Changes**

1.  **Save the changes** to your website's HTML file. Here is an example of what all the addittions should look like once added together:
    
    <br />
    
    ```
    &lt;script&gt;
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
            &lt;/script&gt;
    
            &lt;script&gt;
              function TruendoCookieControlCallback(cookieObj) {
                if (cookieObj.preferences) {
                  gtag("consent", "update", {
                    preferences: "granted",
                  });
                } else {
                  gtag("consent", "update", {
                    preferences: "denied",
                  });
                }
                if (cookieObj.marketing) {
                  gtag("consent", "update", {
                    ad_storage: "granted",
                    ad_personalization: "granted",
                    ad_user_data:"granted",
                  });
                } else {
                  gtag("consent", "update", {
                    ad_storage: "denied",
                    ad_personalization: "denied",
                    ad_user_data:"denied",
                  });
                }
                if (cookieObj.statistics) {
                  gtag("consent", "update", {
                    analytics_storage: "granted",
                  });
                } else {
                  gtag("consent", "update", {
                    analytics_storage: "denied",
                  });
                }
                if (cookieObj.social_content) {
                  gtag("consent", "update", {
                    social_content: "granted",
                  });
                } else {
                  gtag("consent", "update", {
                    social_content: "denied",
                  });
                }
                if (cookieObj.social_sharing) {
                  gtag("consent", "update", {
                    social_sharing: "granted",
                  });
                } else {
                  gtag("consent", "update", {
                    social_sharing: "denied",
                  });
                }
              }
              &lt;/script&gt;
    
            &lt;!-- TRUENDO Privacy Center --&gt;
            &lt;script id="truendoAutoBlock" type="text/javascript" src="https://cdn.priv.center/pc/truendo_cmp.pid.js" data-siteid="YOUR SITE ID"&gt;&lt;/script&gt;
            &lt;!-- End TRUENDO Privacy Center --&gt;
    
            &lt;!-- Google tag (gtag.js) --&gt;
            &lt;script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXX"&gt;&lt;/script&gt;
            &lt;script&gt;
              window.dataLayer = window.dataLayer || [];
              function gtag() { dataLayer.push(arguments); }
              gtag('js', new Date());
    
              gtag('config', 'G-xxxxxxxx');
            &lt;/script&gt;
    ```
    

## Advanced Consent Mode

By following **all** the above steps you have already successfully implemented **Advanced Consent Mode** with Google Analytics using the TRUENDO Consent Management Platform. Click here to find out how to test if everything is working as it should be. Proceed to the next section to configure **Basic Consent Mode.**

<br />

## Basic Consent Mode

**Step1**

Please follow all the above steps before proceding with the rest of this guide.

<br />

**Step 2: Log into TRUENDO**

Log in to your existing TRUENDO account. If you don't have an account yet, you'll need to [create one](console.truendo.com).

<br />

**Step 3: Navigate to Services**

Once logged in, go to the **TRUENDO Console**. Click on **Services** on the left sidebar. Scroll through your list of services or use the search function to find **Google Analytics**.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/e8BgSg2qbtL9ewkRUema.png"></figure>

<br />

**Step 4: Open Google Analytics Service**

Click on the **Google Analytics** service. This action will open the Service Details menu on the right side of your screen.

<br />

**Step 5: Access Additional Identifier Settings**

Scroll to the bottom of the Service Details menu and expand the **Additional Identifier Settings**.

<br />

**Step 6: Switch Script State**

In the **Script Details** section, switch the state from **‘Applied’** to **‘Available’**.

<br />

**Step 7: Apply Necessary Scripts**

Look for any scripts that haven't been applied yet. Click on the three dots next to any script displayed and select the **Apply** option.

<br />

**Step 8: Confirm Script Application**

An **Apply Identifier** popup will appear. Click on **Apply** and then refresh your page.

<br />

**Step 9: Repeat Script Application**

Repeat Steps 7 and 8 until all available scripts have been applied.

<br />

**Step 10: Publish Changes**

After applying all the necessary scripts, click on **Publish** at the top of your screen to save your changes.

And that’s it! You’ve successfully set up Basic Consent Mode with Google Analytics using TRUENDO. Enjoy the peace of mind that comes with knowing your site is compliant with data privacy regulations. If you have any questions or encounter any issues, don’t hesitate to reach out for support. Happy tracking!

<br />

Remember if you would like to see more details on any of the above steps you can have a look at our [documentation](http:#?target=SAL-PF6J-EMH-GQE) section on TRUENDO and Google Consent Mode aswell.

<br />