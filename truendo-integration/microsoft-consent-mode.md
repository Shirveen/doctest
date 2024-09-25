---
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Microsoft Consent Mode'
id: 1ZG-BH6Q-B4Z-WMY
slug: microsoft-consent-mode
isVisible: true
lastUpdated: '2024-09-23 13:03:50'
---
FIND PAGE SEND TO JOSH<br />
<br />
Hello for now we have come up with a solution such that you can get set up while we still prepare the docs.

This is assuming you have followed the initial instructions from Microsoft on inserting the the UET tag.

Now also assuming you are using GTM (feel free to correct me)

Create a custom Tag in GTM containing the following:

&lt;script&gt;

window.uetq = window.uetq || \[\];

window.uetq.push('consent', 'default', {

'ad\_storage': 'denied'

});

&lt;/script&gt;

&lt;script&gt;

function TruendoCookieControlCallback(cookieObj) {

if (cookieObj.marketing) {

window.uetq.push("consent", "update", {

ad\_storage: "granted",

});

} else {

window.uetq.push("consent", "update", {

ad\_storage: "denied",

});

}

}

&lt;/script&gt;

The first above sets the default UET consent state and the callback allows that this state is updated based on consent from TRUENDO.

VERY IMPORTANT:

in GTM please adjust your Tag ordering such that this tag fires before the TRUENDO tag.

If you need any further assistance please let me know.