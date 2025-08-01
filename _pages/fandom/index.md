---
title: "연성 노트"
layout: single
permalink: /fandom/
---

# 연성 노트

역사 속 인물과 사건에서 영감을 받아 만든 2차 창작 아이디어와 세계관 노트를 기록합니다.

- [연성기록실](/fandom/novel)
- [캐릭터 구상 및 해석](/fandom/characters/)

---

## 🆕 최신 포스트 (디버깅 포함)

### 연성기록실 (fandom/novel)
{% comment %}
포스트 목록 중 novel 카테고리를 가진 것만 필터링
배열에서 문자열 검색 오류 방지를 위해 join 사용
{% endcomment %}
{% assign novel_posts = site.posts | where_exp: "post", "post.categories | join: ',' | contains: 'novel'" | limit: 3 %}

{% if novel_posts.size > 0 %}
{% for post in novel_posts %}
- [{{ post.title }}]({{ post.url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
{% else %}
> ⚠️ 디버그: `novel` 카테고리 포스트가 없습니다.
{% endif %}

<p><a href="/fandom/novel/" class="btn btn--primary">더보기 →</a></p>

---

### 캐릭터 해석 (fandom/characters)
{% assign characters_posts = site.posts | where_exp: "post", "post.categories | join: ',' | contains: 'characters'" | limit: 3 %}

{% if characters_posts.size > 0 %}
{% for post in characters_posts %}
- [{{ post.title }}]({{ post.url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
{% else %}
> ⚠️ 디버그: `characters` 카테고리 포스트가 없습니다.
{% endif %}

<p><a href="/fandom/characters/" class="btn btn--primary">더보기 →</a></p>

---

## 🔍 디버깅: 전체 포스트와 카테고리
{% for post in site.posts %}
- {{ post.title }} → 카테고리: {{ post.categories | join: ', ' }}
{% endfor %}
