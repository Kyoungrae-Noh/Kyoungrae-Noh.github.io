---
layout: default
title: "Kyoungrae Noh Blog"
---

<div class="container">
  <!-- 🔹 상단 네비게이션 바 -->
  <nav>
    <ul>
      <li><a href="{{ site.baseurl }}/">ALL</a></li>
      {% for category in site.categories %}
        <li><a href="{{ site.baseurl }}/category/{{ category[0] }}">{{ category[0] | capitalize }}</a></li>
      {% endfor %}
    </ul>
  </nav>

  <!-- 🔹 포스트 리스트 -->
  <div class="post-list">
    {% for post in site.posts %}
      <div class="post-card">
        <a href="{{ post.url | relative_url }}">
          {% if post.image %}
            <img src="{{ post.image }}" alt="Post Image">
          {% endif %}
          <div class="post-info">
            <h2>{{ post.title }}</h2>
            <p class="date">{{ post.date | date: "%Y-%m-%d" }} &nbsp; — &nbsp; {{ post.read_time }} min read</p>
            <p class="excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
          </div>
        </a>
      </div>
    {% endfor %}
  </div>

  <!-- 🔹 사이드바 (프로필 및 연락처) -->
  <aside class="sidebar">
    <img src="/assets/profile.jpg" alt="Profile Image">
    <h3>Kyoungrae Noh</h3>
    <p>AI Researcher in Computer Vision</p>
    <ul class="social-links">
      <li><a href="https://linkedin.com/in/kyoungrae-noh">LinkedIn</a></li>
      <li><a href="https://github.com/Kyoungrae-Noh">GitHub</a></li>
      <li><a href="mailto:kyoungrae.noh@example.com">Email</a></li>
    </ul>
  </aside>
</div>
