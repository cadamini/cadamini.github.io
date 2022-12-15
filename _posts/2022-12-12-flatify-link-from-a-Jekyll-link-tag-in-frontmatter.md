---
layout: post
title:  "Including a link tag in the front matter"
image: https://cdn-icons-png.flaticon.com/512/3858/3858629.png
categories: [ Jekyll ]
tags: [ Stackoverflow ]
featured: false
author: christian
banner-bottom: This is a [Link to this post]({% link _posts/2022-12-12-flatify-link-from-a-Jekyll-link-tag-in-frontmatter.md %}) using a Jekyll link tag in the page's front matter.
---

For [this Stackoverflow question](https://stackoverflow.com/questions/74776719/jekyll-link-inside-a-variable-called-from-a-markdown-file/74777614#74777614), I could add ansnwer because I have found this [blog post](http://acegik.net/blog/ruby/jekyll/plugins/howto-nest-liquid-template-variables-inside-yaml-front-matter-block.html) some time ago. The question was how to add a link inside a variable in the front matter.

## 1. Create a filter plugin

{% raw %}
```
# file: _plugins/expand_nested_variable_filter.rb

module Jekyll
  module ExpandNestedVariableFilter
    def flatify(input)
      Liquid::Template.parse(input).render(@context)
    end
  end
end

Liquid::Template.register_filter(Jekyll::ExpandNestedVariableFilter)
```
{% endraw %}

## 2. Apply the filter

{% raw %}
```
---
layout: post
title:  "Title"
date:   2022-12-06 18:26:05 +0100
categories: category
author: Author name
author-pic: author.jpg
banner-bottom: [Link to this post]({% link 2022-12-12-flatify-link-from-a-Jekyll-link-tag-in-frontmatter.md %}) using a Jekyll link tag in the page's front matter.
---

{{ site.baseurl | flatify }}
```
{% endraw %}

## The result

The link tag in the front matter displayed above is properly converted into a link in the content: 

{{ page.banner-bottom | flatify }}
