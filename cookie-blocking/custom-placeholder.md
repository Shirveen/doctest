---
description: "Learn how to create a custom placeholder for your content using TRUENDO. Follow step-by-step instructions to ensure proper integration and compliance. Last updated June 19, 2024.\n"
keywords:
    - TRUENDO
    - 'Custom Placeholder'
    - 'iFrame Placeholder'
    - 'Cookie Management'
    - 'Data Privacy'
    - 'User Consent'
canonical_url: 'https://docs.truendo.com/custom-placeholder'
og_title: 'Creating a Custom Placeholder - TRUENDO Documentation'
og_description: "Follow our guide to create a custom placeholder for your content using TRUENDO. Ensure proper integration and compliance with detailed instructions.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-19'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Custom Placeholder'
id: AYA-NW3J-DPP-86Q
slug: custom-placeholder
isVisible: true
lastUpdated: '2024-06-21 08:17:09'
---
# <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Creating a custom placeholder</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">To create a custom placeholder you need to create a separate file that you can use as the </span></span> `src` for the script or iFrame of your content.

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Below you will find a basic structure for a placeholder:</span></span>

[<span style="color:rgb(0, 85, 187);"><span style="background-color:rgb(255, 255, 255);">placeholder.html</span></span>](https://truendo-file-hosting.s3.eu-central-1.amazonaws.com/placeholder_en.html)

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 1</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Create a HTML file in your web project called </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">placeholder.html</span></span>**

The placeholder filename **MUST contain** the word _placeholder_ all in lowercase

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 2</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Copy the code above and add your custom styling within </span></span> `&lt;style&gt;` tags. Alternatively you can add a `&lt;link&gt;` tag to a CSS file of your choosing.

> <div class="sd-callout" data-callout-type="info"><p><strong>Note:</strong> It is possible to change the text of the placeholder. However if the user is not informed correctly about what they are accepting the placeholder can become non-compliant with the GDPR</p></div>

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 3</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Now we need to change the source attribute of the iFrame for the embedded content:</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Change the </span></span> `src` attribute of the iFrame which you are embedding to `data-src`. Add the attribute `data-trucookiecontrol`. This attribute has to be set to the corresponding category. For example `"social_content"`. Add the attribute `truendo="true".`

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Your code could look similar to this:</span></span>

`&lt;iframe data-trucookiecontrol="social_content" truendo="true" data-src="[...orginal source]"&gt;&lt;/iframe&gt;`

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 4</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Now all we have to do is add a </span></span> `src` attribute that links to the custom placeholder. Make sure the `src` attribute leads to the **placeholder.html** file we just created. The TRUENDO placeholder templates accept multiple attributes:

-   **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">domain</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">You can enter the name of you business or of your website URL here. This will be displayed in the placeholder.</span></span>
-   **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">category_name</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">The written name of the category, like: </span></span> `"Social Content"` for the category `"social_content"`
-   **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">category_id</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">The ID of the cookie category which you have selected for the embedded content, like: </span></span> `"social_content"`

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">The above attributes need to be added as query parameters to the URL of the iFrame.</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Example: </span></span> `src="https://www.example.com/placeholder.html?domain=truendo.com&category_id=social_content&category_name=Social%20Content"`

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">The result should look similar to this:</span></span>

```html
<iframe data-trucookiecontrol="social_content" src="https://www.example.com/placeholder.html?domain=truendo.com&category_id=social_content&category_name=Social%20Content" truendo="true" data-src="[...orginal source]"></iframe>
```

> <div class="sd-callout" data-callout-type="info"><p><strong>Important Note:</strong> Content that falls under the necessary category should not be changed as these can run without consent.</p></div>

<br />