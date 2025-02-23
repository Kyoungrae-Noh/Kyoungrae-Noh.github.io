---
layout: default
title: "Kyoungrae Noh Blog"
---

<h1>📌 Latest Posts</h1>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%Y-%m-%d" }}
    </li>
  {% endfor %}
</ul>
