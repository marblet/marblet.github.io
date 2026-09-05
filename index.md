---
layout: default
title: Home
---

# marblet.github.io

## Articles

<ul>
  {% assign article_pages = site.pages | sort: "path" %}
{% for page in article_pages %}
{% unless page.path == "index.md" %}
<li>
<a href="{{ page.url | relative_url }}">
{{ page.title | default: page.name }}
</a>
</li>
{% endunless %}
{% endfor %}
</ul>
