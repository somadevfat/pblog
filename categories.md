---
layout: default
title: カテゴリ一覧
---

<h1>カテゴリ一覧</h1>

<div class="category-list">
  {% for category in site.categories %}
    <div class="category-item">
      <h2 id="{{ category[0] | slugify }}">{{ category[0] }}</h2>
      <ul class="post-list-by-cat">
        {% for post in category[1] %}
          <li>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            <span class="post-date">{{ post.date | date: "%Y年%m月%d日" }}</span>
          </li>
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</div> 