---
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'Content Security Policy Configuration'
id: LI7-ULL9-KB7-YRZ
slug: content-security-policy-configuration
isVisible: true
lastUpdated: '2024-08-27 12:44:49'
---
# Configuring your Content Security Policy (CSP) to work with TRUENDO

If you make use of a CSP, you must configure it to allow resources from specific TRUENDO URLs. TRUENDO uses these URLs for its scripts, images, styles, fonts, and frames.

<br />

### Required URLs for CSP

Add the following URLs to your CSP settings:

-   `https://*.truendo.com`
-   `https://*.priv.center`

### Instructions

1.  **Access your CSP Settings**: Depending on your Content Management System (CMS) or server configuration, locate the section where you can modify or add your CSP settings.
2.  **Update CSP**: Add the following directives to your CSP configuration to allow TRUENDO to load its resources properly:
    
    ```
    script-src https://\*.truendo.com https://\*.priv.center;
    img-src https://\*.truendo.com https://\*.priv.center;
    style-src https://\*.truendo.com https://\*.priv.center;
    font-src https://\*.truendo.com https://\*.priv.center;
    frame-src https://\*.truendo.com https://\*.priv.center;
    ```
    
3.  **Save and Test**: Save your changes and test your website to ensure that TRUENDO is functioning correctly and that no resources are being blocked.

### Additional Information

By including these URLs in your CSP settings, you ensure that all TRUENDO resources, including scripts, images, styles, fonts, and frames, are loaded without issues, allowing the consent management platform to operate smoothly on your website.

<br />