---
layout: post
title:  "Working with Markdown"
categories: [ Markdown ]
tags: [ Tutorial ]
image: assets/images/16.jpg
---

This post contains useful markdown syntax that will help you  in the future. The examples are not displayed in HTML but Markdown because I use `~~~` around them. 

## Headings

~~~
# h1 heading
## h2 heading
### h3 heading
~~~

## Bold and italics

~~~
**This text is bold**
*And this italics*
~~~

## Special formatting

Use special formatting when the need arises:

~~~
- ~~strike through this text~~
- ==highlight this text== text
- \*escaped characters in this text instead showing text in italics\*
~~~

## Links

~~~
[this is a link](to this file or URL)
~~~

## Images

~~~
![this is the alt text](for the image in this location)
~~~

## Writing code blocks

You can insert two types of code elements in Markdown:
- Inline code within a line of text: Wrap any word or words in back-ticks (`):

    ~~~
    Create a `code snippet` like this.
    ~~~

- Larger code snippets in code blocks: Use triple back ticks (```)

    ~~~
    ```
    .my-link {
        text-decoration: underline;
    }
    ```
    ~~~

You can implement code highlighting for different languages, for example HTML: 

HTML: 

~~~
```html
<li class="ml-1 mr-1">
    <a target="_blank" href="#">
    <i class="fab fa-twitter"></i>
    </a>
</li>
```
~~~
