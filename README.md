# Zenn CLI

* [📘 How to use](https://zenn.dev/zenn/articles/zenn-cli-guide)
---

# ✨ Zenn Content Repository

[![Zenn](https://badgen.org/img/zenn/zenn.dev/kitakitao/articles?icon=zap\&label=Zenn)](https://zenn.dev/)
このリポジトリは **Zenn CLI** を利用して、Zenn に記事や本を公開するためのコンテンツを管理しています。
Markdown で執筆し、GitHub に push するだけで Zenn に反映されます 🚀

---

## 📂 ディレクトリ構成

```
.
├── articles/    # 記事 (Markdown)
├── books/       # 本（連載記事）
└── README.md    # このファイル
```

---

## 🛠 セットアップ

### 必要環境

* Node.js v18+（LTS 推奨）
* npm または yarn

```bash
node -v
npm -v
```

nvm 推奨:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
nvm install --lts
nvm use --lts
```

---

## ✍️ 記事を書く

### 初期化（最初だけ）

```bash
npx zenn init
```

### 新規記事

```bash
npx zenn new:article --slug first-article
```

例: `articles/first-article.md`

### 新規本（シリーズ記事）

```bash
npx zenn new:book --slug first-book
```

---

## 👀 プレビュー

```bash
npx zenn preview
```

* `http://localhost:8000` で記事をリアルタイム確認
* VS Code で編集すると即時反映

---

## 🔄 公開フロー

1. 記事や本を編集
2. コミット & プッシュ

```bash
git add .
git commit -m "Add: first article"
git push origin main
```

3. GitHub 連携済みなら、自動で Zenn に反映 🎉

---

## 🎯 フロントマター例

```md
---
title: "はじめてのZenn"
emoji: "🔥"
type: "tech"     # tech: 技術記事 / idea: アイデア
topics: ["zenn", "setup"]
published: true  # 公開: true / 非公開: false
---
```

---

## 📌 チートシート (Zenn CLI)

| コマンド                                 | 説明      |
| ------------------------------------ | ------- |
| `npx zenn init`                      | 初期化     |
| `npx zenn new:article --slug <slug>` | 記事作成    |
| `npx zenn new:book --slug <slug>`    | 本作成     |
| `npx zenn preview`                   | プレビュー開始 |

---

## 📝 Markdown 記法チートシート

### 見出し

```md
# 見出し1
## 見出し2
### 見出し3
```

### 強調

```md
**太字**
*斜体*
~~打ち消し~~
```

### リスト

```md
- 箇条書き
- リスト
  - ネスト

1. 番号付き
2. リスト
```

### コード

````md
`インラインコード`

```bash
# コードブロック（bash）
echo "Hello Zenn"
````

````

### 引用
```md
> これは引用です
````

### リンク & 画像

```md
[Zenn](https://zenn.dev)
![代替テキスト](https://placehold.jp/150x100.png)
```

### 表

```md
| 見出し1 | 見出し2 |
|---------|---------|
| 内容A   | 内容B   |
| 内容C   | 内容D   |
```

### 注釈

```md
本文テキスト[^1]

[^1]: 注釈の説明文
```

---

## 💡 運用Tips

* **公開/非公開**は `published:` で制御
* 記事は **Markdown で軽量管理**
* プライベートメモや下書きも同じリポジトリで管理OK
* GitHub Actions 等で自動管理も拡張可能

---

> ✨ 執筆して push → Zenn に公開。
> シンプルかつ効率的な記事管理を実現します。

---