---
layout: default
title: ホーム
---

# pblogへようこそ！

このブログは技術解説とプログラミング学習の記録を残す場所です。

## このブログについて

- **目的**: 技術解説とプログラミング学習のアウトプット
- **対象**: プログラミング初心者〜中級者
- **内容**: Java、Web開発、プログラミング基礎など

## 最新記事

{% if site.posts.size > 0 %}
<div class="post-list">
  {% for post in site.posts limit:5 %}
    <article class="post-item">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y年%m月%d日" }}</time>
        {% if post.categories.size > 0 %}
        · {{ post.categories | join: ", " }}
        {% endif %}
      </p>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    </article>
  {% endfor %}
</div>

{% if site.posts.size > 5 %}
<p class="all-posts-link">
  <a href="{{ '/posts/' | relative_url }}">すべての記事を見る &rarr;</a>
</p>
{% endif %}

{% else %}

まだ記事はありませんが、今後以下のような内容を投稿予定です：

- Java基礎解説
- Spring Boot入門
- Git/GitHub使い方
- プログラミング学習方法
- 技術書レビュー

{% endif %}

## お知らせ

ブログを開設しました！（{{ "now" | date: "%Y年%m月%d日" }}）

---

定期的に記事を更新していく予定です。お楽しみに！ 