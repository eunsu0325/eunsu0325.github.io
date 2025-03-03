---
layout: single
title: "CNN"
permalink: /tags/cnn/
taxonomy: tags
term: "cnn"
author_profile: true
---

<style>
/* 페이지 전체를 가운데 정렬 (가로 폭 고정) */
.my-tag-container {
  max-width: 700px;  /* 원하는 최대 폭 */
  margin: 0 auto;    /* 좌우 여백 자동 → 중앙 정렬 */
  text-align: left;  /* 텍스트는 왼쪽 정렬 */
}
</style>

<div class="my-tag-container">
  <h1></h1> 

  {% assign tag_posts = site.posts | where_exp: "post", "post.tags contains page.term" %}
  
  {% if tag_posts == empty %}
    <p>No posts found for tag "{{ page.term }}".</p>
  {% else %}
    {% for post in tag_posts %}
      <article>
        <!-- 글 제목만 -->
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>

        <!-- 날짜 (선택) -->
        <time datetime="{{ post.date | date_to_xmlschema }}">
          {{ post.date | date: "%Y-%m-%d" }}
        </time>
      </article>
    {% endfor %}
  {% endif %}
</div>
