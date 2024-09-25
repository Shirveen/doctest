---
meta_description: "Learn how to connect iFrames to the TRUENDO Privacy Widget. Add necessary attributes to ensure proper cookie control and user consent. Last updated June 19, 2024.\n"
keywords:
    - TRUENDO
    - iFrames
    - 'Privacy Widget'
    - 'Cookie Management'
    - 'Data Privacy'
    - 'User Consent'
canonical_url: 'https://docs.truendo.com/connecting-iframes'
og_title: 'Connecting iFrames to the Privacy Widget - TRUENDO Documentation'
og_description: "Follow our guide to connect iFrames to the TRUENDO Privacy Widget. Ensure proper cookie control and user consent with the necessary attributes.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-19'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Advanced Consent Mode with Google Analytics'
id: CXX-SK39-HDP-269
slug: advanced-consent-mode-with-google-analytics
isVisible: true
lastUpdated: '2024-06-21 08:14:23'
---
# **Implementing Advanced Consent Mode with Google Analytics**

<br />

<div class="sd-callout" data-callout-type="alert"><p>This is for <strong>users that</strong> <strong>do not use GTM to integrate Google analytics. </strong>If you use GTM please click <a href="http:#?target=RRK-AEO3-EIM-GWV" target="_self">here</a></p></div>

### **<span style="color:black;">Step 1</span>**

<span style="color:black;">Paste the following snippet in the </span> `&lt;head&gt;` <span style="color:black;">as the </span> **<span style="color:black;">very first script</span>**<span style="color:black;">, on the page section of your website. </span> <span style="color:#0A0A0A;">Ensure that this is first script, before all other scripts, including any Google Analytics scripts and other TRUENDO scripts.</span>

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

        <script>
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
          </script>
```

### **<span style="color:black;">Step 2</span>**

[<span style="color:#0055BB;">Create a TRUENDO account</span>](https://console.truendo.com/) <span style="color:#0A0A0A;">or log in to an existing one.</span>

### **<span style="color:black;">Step 3</span>**

<span style="color:black;">In the TRUENDO Console, click on </span> **<span style="color:black;">Banner </span>** <span style="color:black;">on the left sidebar then scroll down to </span> **<span style="color:black;">Integration via Script</span>**<span style="color:black;">.</span>

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/0jE3PoizxpZ6KjGnGT3l.png"></figure>

<span style="color:black;">Copy your snippet, which will look something like this:</span>

```
        <!-- TRUENDO Privacy Center -->
        <script id="truendoAutoBlock" type="text/javascript" src="https://cdn.priv.center/pc/truendo_cmp.pid.js" data-siteid="YOUR SITE ID"></script>
        <!-- End TRUENDO Privacy Center -->
```

### **<span style="color:black;">Step 4</span>**

<span style="color:black;">Paste the snippet in the </span> `&lt;head&gt;` **<span style="color:black;">immediately</span>** <span style="color:black;">after the scripts that were pasted in </span> **<span style="color:black;">Step 1</span>**<span style="color:black;">, on the page section of your website.</span>

### **<span style="color:black;">Step 5</span>**

<span style="color:black;">You may now copy the script that you get from Google Analytics directly in the </span> `&lt;head&gt;` **<span style="color:black;">immediately</span>** <span style="color:black;">after the scripts that were pasted in </span> **<span style="color:black;">Step 1 </span>** <span style="color:black;">and</span> **<span style="color:black;">Step 4</span>**<span style="color:black;">. See the example below of what your </span> `&lt;head&gt;` <span style="color:black;">should look like at this point:</span>

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

        <script>
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
          </script>

        <!-- TRUENDO Privacy Center -->
        <script id="truendoAutoBlock" type="text/javascript" src="https://cdn.priv.center/pc/truendo_cmp.pid.js" data-siteid="YOUR SITE ID"></script>
        <!-- End TRUENDO Privacy Center -->

        <!-- Google tag (gtag.js) -->
        <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXX"></script>
        <script>
          window.dataLayer = window.dataLayer || [];
          function gtag() { dataLayer.push(arguments); }
          gtag('js', new Date());

          gtag('config', 'G-xxxxxxxx');
        </script>
```

### Step 6

<span style="color:black;">Save your changes</span>**<span style="color:black;">.</span>**

<span style="color:black;">You are done.</span>