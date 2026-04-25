# Bookshelf — Library セクション用データ

> 「いま自分を作っているもの」を記録する作業ファイル。
> ここに書き溜めたものが、後で Library セクションのデータになります。
> 最初は **Influences (自分を作ったもの)** から埋めるのが楽。

---

## 構造

```
📖 BOOKS         🎧 LISTENING
├─ 古典           ├─ YouTube
├─ 実用書         └─ Podcast
├─ 小説
└─ 漫画

各カテゴリ × 3 つのステータス:
  ▸ Now            (今読んでる/聴いてる)  — 1〜2件
  ▸ Influences     (自分を作った)         — 3〜5件
  ▸ Reread / Re-listen (何度も)          — 3〜5件
```

各アイテム: `タイトル / 著者 or チャンネル / "なぜ好きか" 1行`

---

## 📖 古典 (Classics)

### Now
- *(未記入)*

### Influences
- **人生の短さについて** / セネカ / 「忙しさは生きていることではない、と気づかされた一冊。サイトの北極星。」 ← 確定
- *(未記入)*
- *(未記入)*

### Reread
- *(未記入)*
- *(未記入)*

---

## 📖 実用書 (Practical)

### Now
- *(未記入)*

### Influences
- *(未記入)*
- *(未記入)*
- *(未記入)*

### Reread
- *(未記入)*
- *(未記入)*

---

## 📖 小説 (Fiction)

### Now
- *(未記入)*

### Influences
- *(未記入)*
- *(未記入)*
- *(未記入)*

### Reread
- *(未記入)*
- *(未記入)*

---

## 📖 漫画 (Manga)

### Now
- *(未記入)*

### Influences
- *(未記入)*
- *(未記入)*
- *(未記入)*

### Reread
- *(未記入)*
- *(未記入)*

---

## 🎧 YouTube

### Always-on (いつも見ている)
- *(未記入)* / チャンネル名 / "なぜ"
- *(未記入)*
- *(未記入)*

### Recently obsessed (最近ハマってる)
- *(未記入)*
- *(未記入)*

---

## 🎧 Podcast

### Always-on (いつも聴いている)
- *(未記入)*
- *(未記入)*
- *(未記入)*

### Recently obsessed (最近ハマってる)
- *(未記入)*
- *(未記入)*

---

## 記入ガイド

- **書き方の例**:
  ```
  - **Sapiens (サピエンス全史)** / Yuval Noah Harari / 「『虚構を信じる力』が人類の本質という指摘で、起業の見方が変わった。」
  ```
- 「なぜ好きか」は **必ず1行** に収める (棚で並んだときの読みやすさ重視)
- 完璧じゃなくて OK。あとで書き直せるし、半年に1回見直す前提で。
- 「これ書くの恥ずかしいかも」と思った本ほど、人柄が出る (例: 中学のときハマった漫画)
- 漫画と古典が同じページに並ぶことが、川染さんらしさの証明になる

## 開発時のデータ構造案 (実装フェーズ用)

```ts
type LibraryItem = {
  id: string;
  category: 'classic' | 'practical' | 'fiction' | 'manga' | 'youtube' | 'podcast';
  status: 'now' | 'influence' | 'reread';
  title: string;
  author: string;          // YouTube/Podcast の場合は channel/host
  why: string;             // 1行
  url?: string;            // 公式リンク
  cover?: string;          // 表紙/サムネイル画像 (任意)
  quote?: string;          // 引用 (任意、本文中に挿入されうる)
};
```
