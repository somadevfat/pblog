# pblog

技術解説とプログラミング学習のブログサイトです。

## 概要

このリポジトリはGitHub Pagesを使用してホストされる技術ブログです。
Jekyllを使用してマークダウンファイルから静的サイトを生成しています。

## サイトURL

https://somadevfat.github.io/pblog

## 構成

- `_config.yml` - Jekyll設定ファイル
- `index.md` - ホームページ
- `_posts/` - ブログ記事（日付-タイトル.md形式）
- `_layouts/` - ページレイアウト
- `assets/` - CSS、画像などの静的ファイル

## 記事の追加方法

1. `_posts/`ディレクトリに `YYYY-MM-DD-title.md` 形式でファイルを作成
2. ファイルの先頭に以下のFront Matterを追加：

```yaml
---
layout: post
title: "記事タイトル"
date: YYYY-MM-DD
categories: [カテゴリ]
tags: [タグ1, タグ2]
---
```

3. その下にマークダウンで記事内容を記述
4. commitしてpushするとGitHub Pagesで自動公開

## ローカル開発

```bash
bundle exec jekyll serve
```

## ライセンス

MIT License 