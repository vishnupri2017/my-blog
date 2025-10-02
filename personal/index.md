---
layout: default
title: 'Personal'
permalink: /personal/
---

<h1>{{ page.title }}</h1>

{% assign personal_posts = site.categories.personal %}
{% if personal_posts %}

<ul>
  {% for post in personal_posts %}
    <li>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p>{{ post.date | date: "%b %-d, %Y" }}</p>
      <div>{{ post.excerpt | strip_html | truncatewords: 40 }}</div>
    </li>
  {% endfor %}
</ul>
{% else %}
<p>No personal posts yet — write one! ✍️</p>
{% endif %}
