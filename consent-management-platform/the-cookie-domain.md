---
description: "Learn how to set the cookie domain in TRUENDO to ensure cookies work across subdomains. Follow step-by-step instructions to avoid banner reappearances and maintain consent status. Last updated June 19, 2024.\n"
keywords:
    - TRUENDO
    - 'Cookie Domain'
    - Subdomains
    - 'Cookie Management'
    - 'Data Privacy'
    - 'Consent Status'
canonical_url: 'https://docs.truendo.com/the-cookie-domain'
og_title: 'The Cookie Domain - TRUENDO Documentation'
og_description: "Follow our guide to set the cookie domain in TRUENDO. Ensure cookies work across subdomains and maintain visitor consent status without banner reappearances.\n"
author: 'TRUENDO Team'
date_modified: '2024-06-19'
robots: 'index, follow'
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: 'The Cookie Domain '
id: QQ1-V9LJ-5M9-16A
slug: the-cookie-domain
isVisible: true
lastUpdated: '2024-06-21 09:37:56'
---
# The Cookie Domain

## The Cookie Domain

To ensure the TRUENDO cookie works across subdomains, you **must** specify the cookie domain that the TRUENDO cookie will be set on. The TRUENDO cookie stores the visitors consent status. If the cookie domain is not specified, TRUENDO will set the cookie domain to the domain the visitor is under when consenting, e.g www.example.com, thus with no cookie domain specified, a cookie will be set just for www.example.com should the visitor proceed to shop.example.com the banner will reappear. In order to avoid this scenario the cookie domain should be set to example.com, this means that the TRUENDO cookie will be available across shop.example.com.

In order to set your cookie domain navigate to the **Banner** section of the menu, scroll down and click on **Advanced** and enter your domain.

<br />

<br />