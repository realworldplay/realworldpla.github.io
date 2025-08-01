---
title: "한국사 아카이브"
layout: single
permalink: /history/
---


이곳은 한국사 연구와 자료를 정리하는 공간입니다.  
조선시대, 고려시대, 삼국시대 그리고 연구 자료실을 통해 다양한 역사적 배경과 인물을 탐구합니다.
시대별 자료 아카이브입니다. 아래에서 각 시대를 선택하세요.

- [조선](/history/joseon/)
- [고려](/history/goryeo/)
- [자료실](/history/resources/)


---

## 🆕 최신 포스트

### 조선
{% assign joseon_posts = site.posts | where_exp: "post", "post.categories contains 'joseon'" | limit: 3 %}
{% for post in joseon_posts %}
- [{{ post.title }}]({{ post.url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}

<p><a href="/history/joseon/" class="btn btn--primary">더보기 →</a></p>

### 자료실
{% assign resources_posts = site.posts | where_exp: "post", "post.categories contains 'resources'" | limit: 3 %}
{% for post in resources_posts %}
- [{{ post.title }}]({{ post.url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}

<p><a href="/history/resources/" class="btn btn--primary">더보기 →</a></p>
