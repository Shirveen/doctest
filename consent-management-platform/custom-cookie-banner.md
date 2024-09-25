---
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Custom Cookie Banner'
id: FGQ-IBXJ-AFE-PC0
slug: custom-cookie-banner
isVisible: true
lastUpdated: '2023-04-06 14:10:51'
---
# <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Custom Cookie Banner Setup</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">In addition to the preset banner styles, Premium users may set up a custom cookie banner. This is a step-by-step guide to build the skeleton structure needed to implement TRUENDO. The rest of the styling must be done by the user.</span></span>

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 1</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">First you need to create a cookie banner structure in your website.</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">This structure must include:</span></span>

-   <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">A container in which all elements are included.</span></span>
    
-   <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Text explaining what the user is accepting.</span></span>
    
-   <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">A button for the “Options”.</span></span>
    
-   <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">A button for the “Necessary Only”.</span></span>
    
-   <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">A button for the “Accept”.</span></span>
    

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">A complete structure in HTML can look like this:</span></span>

```html
<div> <!-- Cookie Banner Container -->
  <!-- Text -->
<h3>Your Privacy</h3>
<p>We use cookies to improve your experience on our site and to show you personalized ads. Click [ACCEPT] to accept
    all cookies, [NECESSARY ONLY] to accept only the necessary cookies or [MY OPTIONS] to find out more about the use of cookies and to change your cookie preferences.</p>
  <!-- Text End -->
<button type="button">My Options</button> <!-- Options Button -->
  <button type="button">Necessary Only</button> <!-- Necessary Only Button -->
  <button type="button">Accept</button> <!-- Accept Button --></div>
```

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 2</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Now you need to add the relevant attributes to the container and the buttons.</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">The container must have the following attributes:</span></span>

`id="cc-banner"` and `style="display:none;"`

> <div class="sd-callout" data-callout-type="info"><strong>Note:</strong> The style attribute can also be added to your CSS file by calling it though the ID as follows:</div>

```css
#cc-banner{
  position: fixed; / Strongly recommended /
  display: none;
}
```

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">For the buttons we must add an onclick attribute each.</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">For the options button: </span></span> `onclick="javascript:Truendo.openCookieSettings()"`

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">For the necessary only button: </span></span> `onclick="javascript:Truendo.acceptNecessaryCookiesOnly()"`

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">For the accept button: </span></span> `onclick="javascript:Truendo.acceptAllCookies()"`

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">When all is done in html, it can look like this:</span></span>

```html
<div id="cc-banner" style="display:none;"> <!-- Cookie Banner Container -->
  <!-- Text -->
<h3>Your Privacy</h3>
<p>We use cookies to improve your experience on our site and to show you personalized ads. Click [ACCEPT] to accept
    all cookies, [NECESSARY ONLY] to accept only the necessary cookies or [MY OPTIONS] to find out more about the use of cookies and to change your cookie preferences.</p>
  <!-- Text End -->
<button type="button" onclick="javascript:Truendo.openCookieSettings()">My Options</button> <!-- Options Button -->
  <button type="button" onclick="javascript:Truendo.acceptNecessaryCookiesOnly()">Necessary Only</button> <!-- Accept Button -->
  <button type="button" onclick="javascript:Truendo.acceptAllCookies()">Accept</button> <!-- Accept Button --></div>
```

> <div class="sd-callout" data-callout-type="tip"><strong>Important Recommendation:</strong> You should put the whole structure within the body tag at a place that is shared by all your pages. For many websites this can be below the footer. If you don’t share any code with your subpages, you have to add the whole structure on every page.</div>

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 3</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">All that is left to do now is to turn on </span></span> `Custom Banner` in your account.

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">To do that you have to </span></span> [<span style="color:rgb(0, 85, 187);"><span style="background-color:transparent;">log in</span></span>](https://console.truendo.com/) to TRUENDO. Make sure the correct domain is selected in the drop down at the top of the main console window. Then go to **Integration** and click on the **Banner** tab. Under **Banner Type** select `Custom Banner` and you are done!

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/eQgVaOjwYNN2KKUruuJD.png"></figure>

<br />

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">You can now proceed to style your banner, however you see fit.</span></span>

<br />

<br />

<br />

<br />