---
description: "Learn how to integrate TRUENDO on your Magento website with our step-by-step guide.  Install the TRUENDO plugin from a zip file and configure it for optimal data privacy management.  Last updated June 18, 2024.\n"
keywords:
    - TRUENDO
    - Magento
    - Integration
    - 'Plugin Installation'
    - 'Data Privacy'
    - 'Cookie Management'
    - 'Website Setup'
canonical_url: 'https://docs.truendo.com/truendo-on-magento'
og_title: 'TRUENDO on Magento - TRUENDO Documentation'
og_description: "Follow our detailed guide to integrate TRUENDO with Magento. Learn to install the plugin from a zip file,  configure settings, and ensure enhanced data privacy.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-18'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: Magento
id: E0S-X8JX-FQU-TS1
slug: magento
isVisible: true
lastUpdated: '2024-06-20 10:50:42'
---
# <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">TRUENDO on Magento</span></span>

## <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Plug-in installation from zip file</span></span>

<br />

1.  <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Download the zip file containing the TRUENDO plugin for Magento </span></span> [<span style="color:rgba(59,103,251,1);"><span style="background-color:rgb(255, 255, 255);">here</span></span>](https://truendo-file-hosting.s3.eu-central-1.amazonaws.com/truendo_cmp-1.0.0.zip)<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>
2.  Create a folder in app/code/truendo/integration
3.  Unzip the .zip file in app/code/truendo/integration
4.  Run the following commands from Magento root directory
    
    to enable the TRUENDO extension:
    
    <br />
    
    ```
    php bin/magento module:enable Truendo_Integration
    php bin/magento setup:upgrade
    php bin/magento setup:di:compile
    php bin/magento cache:clean
    php bin/magento cache:flush
    ```
    
    <br />
    
5.  If your Magento is running in production mode then run the following command:
    
    php bin/magento deploy:mode:set production.
    

<br />

<iframe allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="true" frameborder="0" src="https://www.youtube.com/embed/pZODMFeSX-4?showinfo=0" width="100%"></iframe>

<br />

## Configuration

<br />

1.  Copy your Site-ID from the console under the **Banner** section of the menu under **Integration via Script**.
2.  In Admin navigate to
    
    Stores -&gt; Configuration -&gt; TRUENDO -&gt; Integration Settings
    
3.  Paste your Site-ID in the Input field.

<br />

<br />