---
layout: default
title: タグ一覧
---

<h1>タグ一覧</h1>

<div class="tag-cloud">
{% for tag in site.tags %}
  <a href="#{{ tag[0] | slugify }}" class="tag-name">{{ tag[0] }} ({{ tag[1].size }})</a>
{% endfor %}
</div>

<hr>

<div class="tag-list">
  {% for tag in site.tags %}
    <div class="tag-item">
      <h2 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h2>
      <ul class="post-list-by-tag">
        {% for post in tag[1] %}
          <li>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            <span class="post-date">{{ post.date | date: "%Y年%m月%d日" }}</span>
          </li>
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</div> 