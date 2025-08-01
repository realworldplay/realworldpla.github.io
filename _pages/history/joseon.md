---
title: "조선시대"
layout: single
permalink: /history/joseon/
---

*조선시대*

세종대왕과 집현전부터 조선 후기까지, 역사 속 인물과 사건을 정리합니다.

---

{% include category-with-tags.html category="joseon" %}


<h3>디버깅 출력</h3>
<ul>
  {% for post in site.posts %}
    <li>{{ post.title }} | {{ post.categories }}</li>
  {% endfor %}
</ul>
