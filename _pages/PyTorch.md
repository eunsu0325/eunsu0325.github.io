---
layout: archive
title: "CNN"
permalink: /tags/cnn/   
---

<div class="archive">
  <h1 id="page-title" class="page__title"></h1>
  
  <div class="archive__posts">  
    {%- assign tag_posts = site.posts | where_exp:'post','post.tags contains "cnn"' -%}
    {% if tag_posts == empty %}
      <p>해당 태그(cnn)의 글이 없습니다.</p>
    {% else %}
      {% for post in tag_posts %}  
        <article class="archive__item">
          <!-- 글 제목만 보여주기 -->
          <h2 class="archive__item-title">
            <a href="{{ post.url }}">{{ post.title }}</a>
          </h2>
        </article>
      {% endfor %}
    {% endif %}
  </div>
</div>