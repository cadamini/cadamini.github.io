---
layout: post
title:  "How can I create a multi-page blog post in Jekyll?"
image: /assets/images/806.jpg
description: "How to create a multipage blog post with pagination on top and at the bottom for a sample page with separate layouts for subpages."
categories: [ Jekyll ]
tags: [ Stackoverflow ]
featured: false
author: christian
---

This [Stackoverflow question](https://stackoverflow.com/questions/74813094/how-can-i-create-a-multi-page-blog-post-in-jekyll/74869733#comment132162516_74869733) asked how to create a multipage blog post with pagination and shared this [sample WordPress page](https://shayallenhill.com/ai-generated-palettes/) with separate subpages. 

## Approach

I created a new collection, two layouts, and two include files in Jekyll. 

### Two layouts

Jekyll allows you to add layouts if your HTML structure differs between pages. The page needs two layouts as the start page differs from all other pages on the site. Each layout contains two for loops to create links to the subpages on top and at the bottom. 

### The collection

Jekyll offers posts and collections. In this case, the collection is required to have a folder to store pages and to have links to the single pages.

### Includes

Jekyll has includes for shared content. The pages share some content in different places, e.g. the page about Wes and the other artists, depending on which link you click.

## Code

The Stackoverflow answer shares some code, too. You can find all files in GitHub in this [commit](https://github.com/cadamini/cadamini.github.io/commit/de2921161ad5748c68d99970bf40639245cc5572). Note that I updated the index page to palettes-index later.

## Jekyll result 

This [non-styled example page](https://cadamini.github.io/palettes-index/](https://cadamini.github.io/palettes-index/) should transfer the idea well enough.

---

Post image: <a href="https://www.freepik.com/free-vector/blue-round-modern-annual-report-template_1111040.htm#query=cover&position=2&from_view=keyword">Image by new7ducks</a> on Freepik
