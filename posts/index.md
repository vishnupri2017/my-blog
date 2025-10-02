---
layout: default
title: 'All posts'
permalink: /posts/
---

<h1>{{ page.title }}</h1>

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</p>
      <div>{{ post.excerpt | strip_html | truncatewords: 40 }}</div>
      <p><a href="{{ post.url | relative_url }}">Read more →</a></p>
    </li>
  {% endfor %}
</ul>
