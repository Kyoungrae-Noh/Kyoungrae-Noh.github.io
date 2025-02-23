<img width="958" alt="image" src="https://github.com/user-attachments/assets/630850ca-1e8f-428d-9f76-a9987f7dcd8c" />
---
layout: default
title: "Kyoungrae Noh Blog"
---

<!-- 카테고리 메뉴 -->
<nav>
  <ul>
    <li><a href="{{ '/' | relative_url }}">Home</a></li>
    {% for category in site.categories %}
      <li><a href="{{ category[0] | relative_url }}">{{ category[0] | capitalize }}</a></li>
    {% endfor %}
  </ul>
</nav>

<!-- 최신 포스트 목록 -->
{% for post in site.posts %}
  <div class="post">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p>
      {{ post.date | date: "%Y-%m-%d" }} — {{ post.read_time }} min read
    </p>
    <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
  </div>
{% endfor %}

<!-- 프로필 정보 -->
<hr>
<h3>Kyoungrae Noh</h3>
<p>AI Researcher in Computer Vision</p>
<ul>
  <li><a href="https://linkedin.com/in/your-profile">LinkedIn</a></li>
  <li><a href="https://github.com/Kyoungrae-Noh">GitHub</a></li>
  <li><a href="mailto:your-email@example.com">Email</a></li>
</ul>
