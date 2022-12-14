---
layout: post
title:  "Flatify link from a Jekyll link tag in the front matter"
image: https://cdn-icons-png.flaticon.com/512/3858/3858629.png
description: "My review of a mindfuck of a psychological thriller called Don't Worry Darling"
featured: false
banner-bottom: This is a link using a Jekyll link tag in the page's front matter [link to a page]({{ site.baseurl }}{% link 404.html %}).
---

Test for SO post about Jekyll tags in frontmatter.

{{ page.banner-bottom | flatify }}
