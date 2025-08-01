---
title: "연성기록실"
layout: single
permalink: /fandom/novel/
---

# 연성기록실

역사 속 인물과 사건에서 영감을 받아 만든 2차 창작 소설과 세계관 아이디어를 기록합니다.

---

## 📚 novel 카테고리 포스트 목록
{% assign novel_posts = site.posts | where_exp: "post", "post.categories | join: ',' | downcase | contains: 'novel'" %}
{% if novel_posts.size > 0 %}
<ul>
  {% for post in novel_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span style="font-size: 0.85em; color: #777;">({{ post.date | date: "%Y-%m-%d" }})</span>
      <br>
      <small>카테고리: {{ post.categories | join: ', ' }} | 태그: {{ post.tags | join: ', ' }}</small>
    </li>
  {% endfor %}
</ul>
{% else %}
<p>현재 novel 카테고리의 포스트가 없습니다.</p>
{% endif %}

---

## 🛠 디버깅 출력

### 모든 포스트와 카테고리
<ul>
{% for post in site.posts %}
  <li>{{ post.title }} → {{ post.categories | join: ', ' }}</li>
{% endfor %}
</ul>

---

### novel 카테고리 필터 테스트
<ul>
{% assign debug_novel = site.posts | where_exp: "post", "post.categories | join: ',' | downcase | contains: 'novel'" %}
{% for post in debug_novel %}
  <li>{{ post.title }} ({{ post.categories | join: ', ' }})</li>
{% endfor %}
</ul>
