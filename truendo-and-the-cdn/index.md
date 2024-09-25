---
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: Index
id: IMD-TR9O-3P4-LVR
slug: index
isVisible: true
lastUpdated: '2023-10-16 12:32:41'
---
# TRUENDO and The CDN

## What is  CDN?

 A **Content Delivery Network (CDN)** is a distributed network of servers strategically located in various data centers around the world. The primary purpose of a CDN is to deliver web content, such as text, images, videos, JavaScript files, and other assets, to users more efficiently and with higher performance.

CDNs work by caching and serving content from servers that are geographically closer to the end-users, reducing latency and improving website load times. CDNs are commonly used by websites, e-commerce platforms, streaming services, and any online content provider looking to optimize the delivery of their content to a global audience.

 TRUENDO uses AWS as its CDN,  this allows TRUENDO to run and operate quickly and efficiently no matter where a website visitor is.

What does this mean for:

###  The Website visitor

 A seamless experience where they can interact with the consent request (cookie banner) and TRUENDO Privacy Panel no matter where they are in the world.

### The TRUENDO user (web admin/owner)

 Any changes such as language options, banner styles custom translations etc. may take up to 15 mins to reflect as the CDN nodes need to be repopulated first before delivering the most up to date experience to the web visitor.

 It also means that man Domain checking tools may misinterpret the use of the CDN as traffic or data transfer to the USA, only in the case of a website visitor being in the USA is this true. In all other cases data is NOT transferred to the USA and instead in located in data centers closes to them.

<div class="sd-callout" data-callout-type="alert">please note these tools may also be affected by where they are based ie if the tool is based in the USA then the closest node may be in the USA, this would not be the node that a visitor in another region/country would use.&nbsp;</div>

<br />