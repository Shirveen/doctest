---
description: "Learn how to style your cookie banner with TRUENDO. Customize colors, designs, and display settings to match your website’s aesthetic and compliance needs. Last updated June 19, 2024.\n"
keywords:
    - TRUENDO
    - 'Cookie Banner'
    - 'Banner Styling'
    - Customization
    - 'Privacy Widget'
    - 'Data Privacy'
canonical_url: 'https://docs.truendo.com/styling-your-cookie-banner'
og_title: 'Styling Your Cookie Banner - TRUENDO Documentation'
og_description: "Follow our guide to style your cookie banner with TRUENDO. Customize colors, designs, and display settings to ensure compliance and enhance your website's look.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-19'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Banner Customization'
id: D5O-DVIV-TQQ-IKA
slug: banner-customization
isVisible: true
lastUpdated: '2024-06-21 08:57:21'
---
# Styling Your Cookie Banner

All styling options are located in the main navigation menu in the **Banner** section. You must be both logged in to TRUENDO and have selected the website which you wish to customize.

## Banner Color

Both Essentials and Premium users may change the color of the banner by using the color picker or by entering a specific HEX color code.

<br />

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/h3ZLQbVyL4MiCNHp6lpJ.png"></figure>

<br />

## Displaying the Privacy Widget

Users may also toggle whether to display the Privacy Widget on their pages or not.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/PzusuuQHSzqBBbzEElcO.png"></figure>

<br />

<div class="sd-callout" data-callout-type="alert"><p>The following customization options are <strong>only</strong> available to <strong>Premium</strong> users</p></div>

<br />

## Banner design

Premium users may select from 6 banner designs. Essentials users may only use the Standard Banner design. To preview our banner styles please click [here](https://demo.truendo.com). Premium users can also set up their own [custom design](http:#?target=FGQ-IBXJ-AFE-PC0).

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/gPP8VszgGnYbyh4aCeMl.png"></figure>

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/FCbMvtad44xKdV2DYz68.png"></figure>

<br />

## Banner Display Time Delay

Some users may wish to delay the display of the consent request banner to website visitors. This may be useful if a website has loading animations or other visual features that require a lead-in/play time. This feature is implemented by means of adding an attribute to the TRUENDO script.

To add a delay to the TRUENDO banner popup’s appearance, simply add the following attribute to your TRUENDO script:

`data-popup-delay=“5”`

In this example, the banner appearance will be delayed by 5 seconds, but you can set it from 0 to 10 seconds.

<br />

<div class="sd-callout" data-callout-type="info"><p>It is advisable that this delay is kept as short as possible i.e. just long enough for the animation/visual queue requires to conclude.</p></div>

<br />

The final script will look like this:<br />
<br />
`&lt;!-- TRUENDO Privacy Center --&gt;&lt;script data-popup-delay=“5” id="truendoPrivacyPanel" type="text/javascript" src="https://cdn.priv.center/pc/app.pid.js" data-siteid="YOUR_SITE_ID"&gt;&lt;/script&gt;&lt;!-- End TRUENDO Privacy Center --&gt;`

<br />

## Removing the TRUENDO logo

Premium users can also choose whether to display the TRUENDO logo on their banner or not.

<figure><img src="https://app.snazzydocs.com/storage/users/hEfI2V55cVTdM5ty/docs/G2IomO8914MUXZZJ/images/PZJw3k5WpkD620u8raQh.png"></figure>

<br />