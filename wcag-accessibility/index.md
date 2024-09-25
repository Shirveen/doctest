---
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: Index
id: 4KB-W1SH-SAF-14J
slug: index
isVisible: true
lastUpdated: '2023-10-03 13:02:58'
---
# <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Activating TRUENDO’s WCAG 2.1 Level AAA Compliance</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">In order to activate TRUENDO’s accessibility mode you have to add the following two attributes to the TRUENDO script:</span></span>

`data-accessibility="true"` and `data-transparency="false"`

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">The final script will look like this:</span></span>

```html
<!-- TRUENDO Privacy Center -->
<script data-accessibility="true" data-transparency="false" async="" id="truendoPrivacyPanel" type="text/javascript" src="https://cdn.priv.center/pc/app.pid.js" data-siteid="YOUR_SITE_ID"></script>
<!-- End TRUENDO Privacy Center -->
```

> <div class="sd-callout" data-callout-type="info"><strong>Note:</strong> Be sure to replace <strong>YOURSITEID</strong> with the Site ID of your Domain. You can find your Site ID in your Console. Under <strong>Integration</strong> on the <strong>Integrate to Website</strong> tab.</div>
> 
> <div class="sd-callout" data-callout-type="info"><strong>SEO Note:</strong> WCAG Level AAA requires a<span style="background-color:rgba(115,216,255,1);"> </span><code>&lt;h1&gt;</code><span style="background-color:rgba(115,216,255,1);"> </span>tag in the privacy center. However, Google Webmasters themselves have confirmed that this does not hurt your SEO. <a href="https://www.youtube.com/watch?v=zyqJJXWk0gk" target="_blank"><span style="color:rgb(0, 85, 187);"><span style="background-color:transparent;">Google Webmasters Video</span></span></a></div>

<br />

## Selected Button Color Customization

<br />

To change the color of the border that appears for selecting options **when accessibility mode is enabled**, simply add the following **attribute** to your TRUENDO script:

```
data-accessibility-border-color=“HEXCODE”
```

You can replace HEXCODE with your required color. This can be any color in hexadecimal, these codes are a # (hash) followed by 3 or 6 numbers/letters.

Examples of colors would look like:

`#ff0303` for <span style="color:rgba(255,3,3,1);">Red</span>`<br /> #ffbb00` for <span style="color:rgba(255,187,0,1);">Orange</span>`<br /> #00ffee` for <span style="color:rgba(0,255,238,1);">Light Blue<br></span><br />
You can pick a color with Google’s built in hexadecimal color picker by clicking on this link: [https://www.google.com/search?q=hexidecimal+color+picker](https://www.google.com/search?q=hexidecimal+color+picker)<br />
<br />
The final script will look like this:

```
<!-- TRUENDO Privacy Center -->
<script data-accessibility="true" data-transparency="false" data-accessibility-border-color="#ffbb00" id="truendoPrivacyPanel" type="text/javascript" src="https://cdn.priv.center/pc/app.pid.js" data-siteid="YOUR_SITE_ID"></script>
<!-- End TRUENDO Privacy Center -->
```

<br />