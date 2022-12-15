---
layout: post
title:  "Including a link tag in the front matter"
image: https://cdn-icons-png.flaticon.com/512/3858/3858629.png
featured: false
author: christian
banner-bottom: This is a link using a Jekyll link tag in the page's front matter [link to a page]({{ site.baseurl }}{% link 404.html %}).
---

Test for Stackoverflow post about Jekyll tags in frontmatter.

{{ page.banner-bottom | flatify }}
