---
layout: default
title: 'Code'
permalink: /code/
---

<h1>{{ page.title }}</h1>

{% assign code_posts = site.categories.code %}
{% if code_posts %}

<ul>
  {% for post in code_posts %}
    <li>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p>{{ post.date | date: "%b %-d, %Y" }}</p>
      <div>{{ post.excerpt | strip_html | truncatewords: 40 }}</div>
    </li>
  {% endfor %}
</ul>
{% else %}
<p>No code posts yet — push some code! 💻</p>
{% endif %}
