---
layout: post
title:  "How to add links to an image carousel?"
image: https://t3.ftcdn.net/jpg/01/42/62/84/360_F_142628420_slvDaavEFPE8HKnRc2toe4JWFXLe1DRj.jpg
description: "A question how to add a links to images in a carousel."
categories: [ Jekyll ]
tags: [ Stackoverflow ]
featured: false
author: christian
carousels:
  - images: 
    - image: https://t3.ftcdn.net/jpg/01/42/62/84/360_F_142628420_slvDaavEFPE8HKnRc2toe4JWFXLe1DRj.jpg
      url: https://www.54321.com
    - image: https://thumbs.dreamstime.com/b/tv-test-image-card-rainbow-multi-color-bars-geometric-signals-retro-hardware-s-minimal-pop-art-print-suitable-89603635.jpg
      url: https://www.12345.com
---

To answer [this Stackoverflow question](https://stackoverflow.com/questions/74782155/add-links-to-jekyll-slider-carousel-for-github-pages/74790606?noredirect=1#comment132027196_74790606) (can links be added to the single images of the carousel?) I tested the [Jekyll image carousel](https://jekyllcodex.org/without-plugin/slider/#) from jekyllcodex.org.

This code is adding the carousel: 

`{% include carousel.html height="50" unit="%" duration="7" number="1" %}`

## Page front matter adjustment

I added another url key to the images array:

```
carousels:
- images: 
  - image: /assets/images/image-1.jpg
    url: post-name-1
  - image: /assets/images/image-2.jpg
    url: post-name-2
  - image: /assets/images/image-3.jpg
    url: post-name-3
```

## Text link on the image

Put the link inside the li element: 

{% raw %}
```html
<div class="carousel__track">
  <ul>
    {% for item in page.carousels[number].images %}
      <li class="carousel__slide" style="background-image: url('{{ item.image }}');">
        <a href="{{ item.url }}">{{ item.url }}</a>
      </li>
    {% endfor %}
  </ul>
</div>
```
{% endraw %}

### Text link on the image/slide

The link requires to be a block element: I removed the link text (inline styles for simplicity):

{% raw %}
```html
<div class="carousel__track">
  <ul>
    {% for item in page.carousels[number].images %}
      <li class="carousel__slide" style="background-image: url('{{ item.image }}');">
        <a style="text-decoration:none;display:block;width:100%;height:100%;" href="{{ item.url }}"></a>
      </li>
    {% endfor %}
  </ul>
</div>
```
{% endraw %}
