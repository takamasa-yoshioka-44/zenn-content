# Zenn 記事管理リポジトリ

このリポジトリは[Zenn](https://zenn.dev/)の記事を GitHub と連携して管理するためのリポジトリです。

## 📝 概要

- Zenn CLI を使用してローカルで記事を執筆・プレビュー
- GitHub のリポジトリで記事のバージョン管理
- GitHub から Zenn への自動デプロイ

## 🚀 セットアップ

### 1. Zenn CLI のインストール

```bash
npm install zenn-cli
```

### 2. Zenn アカウントとの連携

1. [Zenn](https://zenn.dev/)にログイン
2. 設定 > GitHub リポジトリ連携から、このリポジトリを連携

### 3. ローカル環境でのプレビュー

```bash
npx zenn preview
```

ブラウザで `http://localhost:8000` にアクセスして記事をプレビューできます。

## 📂 フォルダ構成

```
.
├── articles/          # 記事ファイル（.mdファイル）
├── books/            # 本ファイル（まだ作成していない場合）
├── images/           # 画像ファイル
└── README.md         # このファイル
```

## ✍️ 記事の作成・編集

### 新しい記事の作成

```bash
npx zenn new:article
```

または、手動で `articles/` フォルダに以下の形式でファイルを作成：

```markdown
---
title: '記事のタイトル'
emoji: '📝'
type: 'tech' # tech: 技術記事 / idea: アイデア
topics: ['zenn', 'github']
published: false
---

# 記事の内容をここに書く
```

### 記事ファイル名のルール

- `articles/` フォルダ内に配置
- ファイル名は `[a-z0-9]+` + `.md`
- 例：`my-first-article.md`

## 🌐 記事の公開

### 1. ローカルでの確認

```bash
npx zenn preview
```

### 2. GitHub にプッシュ

```bash
git add .
git commit -m "新しい記事を追加"
git push origin main
```

### 3. Zenn での公開

- `published: true` に変更してプッシュすると自動で公開されます
- Zenn のダッシュボードからも公開設定を変更できます

## 🛠️ 便利なコマンド

| コマンド                 | 説明                 |
| ------------------------ | -------------------- |
| `npx zenn new:article`   | 新しい記事を作成     |
| `npx zenn new:book`      | 新しい本を作成       |
| `npx zenn preview`       | ローカルでプレビュー |
| `npx zenn list:articles` | 記事一覧を表示       |
| `npx zenn list:books`    | 本一覧を表示         |

## 📋 記事作成の Tips

- **絵文字**: 記事にはアイコンとしての絵文字を設定可能
- **トピックス**: 関連する技術タグを 3 つまで設定可能
- **画像**: `images/` フォルダに配置して相対パスで参照
- **下書き**: `published: false` で下書き保存
- **Scrap**: アイデアレベルの内容は type を "idea" に設定

## 🔗 参考リンク

- [Zenn 公式ドキュメント](https://zenn.dev/zenn/articles/zenn-cli-guide)
- [Zenn CLI GitHub](https://github.com/zenn-dev/zenn-editor)
- [GitHub リポジトリ連携について](https://zenn.dev/zenn/articles/connect-to-github)

## 📄 ライセンス

記事の内容については、各記事のライセンス表記に従います。
