---
layout: post
title:  "How can I create a multi-page blog post in Jekyll?"
image: /assets/images/806.jpg
description: "A question how to add a links to images in a carousel."
categories: [ Jekyll ]
tags: [ Stackoverflow ]
featured: false
author: christian
---

This [Stackoverflow question](https://stackoverflow.com/questions/74813094/how-can-i-create-a-multi-page-blog-post-in-jekyll/74869733#comment132162516_74869733) was how to create a multipage blog post with pagination on top and at the bottom for a sample page with separate subpages. 

I created a new collection, two layouts, and some include files in Jekyll. 

## Code and example 

[Code (first version)](https://github.com/cadamini/cadamini.github.io/commit/de2921161ad5748c68d99970bf40639245cc5572) (updated index: index to palettes-index laster)

Here's the resulting example using some hacky, not styled, and not optimized. But at least, it should be good to transfer the idea: 

[https://cadamini.github.io/palattes-index/](https://cadamini.github.io/palettes-index/)

### Two layouts

Jekyll allows you to add layouts if you HTML structure differs between pages. The page needs two layouts as the startpage differs from all other pages in the site. Each layout contains two for loops to create links to the subpages on top and at the bottom. 

### The collection

Jekyll offers posts and collection. In this case, the collection is required to have folder to store pages and to have links to the single pages.

### Includes

Jekyll has includes for shared content. The pages share some content in different places, e.g. the page about Wes and the other artists, depending on which link you click.

---

Post image: <a href="https://www.freepik.com/free-vector/blue-round-modern-annual-report-template_1111040.htm#query=cover&position=2&from_view=keyword">Image by new7ducks</a> on Freepik