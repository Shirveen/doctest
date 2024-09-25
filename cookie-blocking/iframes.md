---
# snazzyDocs - DO NOT REMOVE OR EDIT BELOW THIS LINE
title: iFrames
id: 7TB-2933-UTX-ZR5
slug: iframes
isVisible: true
lastUpdated: '2024-04-12 08:35:32'
---
# <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Connecting iFrames to the Privacy Widget</span></span>

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 1:</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Find the iframe tag in the source/HTML code of your website. If it’s a YouTube video it will look something like this (the iframe may vary depending on the website it comes from).</span></span>

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/a-youtube-video" frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 2:</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Look in </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">line 1</span></span>** <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">of Step 1.<br>Find </span></span> `src` and replace it with `data-src`.

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 3:</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Add</span></span>

```html
data-trucookiecontrol="[category]" truendo="true"
```

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">as attributes, replace </span></span> `[category]` <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">with the technical category name that the content would be classified as, for more info on these categories </span></span> [<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">click here</span></span>](http:#?target=0EB-94M4-TBP-GIU)<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Example:</span></span>

```html
data-trucookiecontrol="social_content" truendo="true"
```

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Step 4:</span></span>

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Add the attribute</span></span>

```html
src="https://cdn.priv.center/pc/placeholder/en/embedded.html"
```

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">to the iframe (this places our default placeholder instead of the content), if you wish to use your own custom placeholder please </span></span> [<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">click here</span></span>](http:#?target=AYA-NW3J-DPP-86Q)<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">.</span></span>

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Before</span></span>

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/a-youtube-video" frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

### <span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">After</span></span>

```html
<iframe width="560" height="315" src="https://cdn.priv.center/pc/placeholder/en/embedded.html" data-src="https://www.youtube.com/embed/a-youtube-video" data-trucookiecontrol="social_content" truendo="true" frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">To finish the process </span></span> **<span style="color:rgb(0, 0, 0);"><span style="background-color:rgb(255, 255, 255);">Save Your Changes</span></span>**