---
layout: post
title:  "Powerful things you can do with the Markdown editor"
categories: [ Markdown ]
tags: [ Tutorial ]
image: assets/images/16.jpg
---

Markdown allows powerful things. If you've gotten pretty comfortable with writing in Markdown, then you may enjoy some more advanced tips.

As with the last post about the editor, you'll want to be actually editing this post as you read it so that you can see all the Markdown code we're using.

## Special formatting

As well as bold and italics, you can also use some other special formatting in Markdown when the need arises, for example:

- ~~strike through~~
- ==highlight==
- \*escaped characters\*

## Writing code blocks

You can insert two types of code elements in Markdown:
- inline: Inline code is formatted by wrapping any word or words in back-ticks:

    ~~~
    `like this`.
    ~~~

- block: Larger code snippets span multiple lines using triple back ticks:

    ```
    .my-link {
        text-decoration: underline;
    }
    ```

You can implement code highlighting for different languages, for example: 

HTML: 

```html
<li class="ml-1 mr-1">
    <a target="_blank" href="#">
    <i class="fab fa-twitter"></i>
    </a>
</li>
```

Ruby:  

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

To be continued ...