---
---

<p>tags here</p> 

<h2>{{ page.title }}</h2>

I created an Artificial Intelligence to produce these palettes ...

<h2>Menu</h2>

<!-- page menu here -->
<ul>
    <li><a href="{{ page.index | relative_url }}">{{ page.title }}</a></li>
    {% for item in page.page_urls %}
        <li><a href="{{ item.url | relative_url }}">{{ item.title }} Palettes</a></li>
    {% endfor %}
</ul>

{{ content }}

<h2>Pages</h2>

<ul>
    <li><a href="{{ page.index | relative_url }}">1</a></li>
        {% for item in page.page_urls %}
            {% assign page_number = forloop.index | plus: 1 %}
        <li><a href="{{ item.url | relative_url }}">{{ page_number }}</a></li>
    {% endfor %}
</ul>
                