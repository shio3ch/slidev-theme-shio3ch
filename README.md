# slidev-theme-shio3ch

Slidev用カスタムテーマ。エメラルドグリーン基調のカラーパレット、手書き風の見出し下線、M PLUS 2フォントが特徴。ダーク/ライトモード対応。

## セットアップ

### テーマ単体で開発

```sh
cd example
deno task dev
```

### 他プロジェクトから利用

```json
{
  "dependencies": {
    "slidev-theme-shio3ch": "github:shio3ch/slidev-theme-shio3ch"
  }
}
```

frontmatter でテーマを指定：

```yaml
---
theme: shio3ch
---
```

---

## レイアウト一覧

### cover

カバースライド。グラデーション背景付き。

```md
---
layout: cover
---
# タイトル
サブタイトル
```

### intro

イントロスライド。cover に似た大きな見出し表示。

```md
---
layout: intro
---
# イントロダクション
```

### section

セクション区切り。中央配置の大きな見出し。`sectionNumber` propで背景に巨大な半透明ナンバーを表示可能。

```md
---
layout: section
sectionNumber: "01"
---
# セクション名
```

### statement

宣言・メッセージ用。太字の中央配置テキスト。

```md
---
layout: statement
---
# 伝えたいメッセージ
```

### fact

数値やファクトを大きく表示。

```md
---
layout: fact
---
# 100%
補足テキスト
```

### quote

引用文の表示。

```md
---
layout: quote
---
# "引用文"
出典
```

### image-right

左にテキスト、右に画像。画像との境界にテーマカラーのラインが入る。

```md
---
layout: image-right
image: https://example.com/photo.jpg
---
# タイトル
- ポイント1
- ポイント2
```

### image-left

左に画像、右にテキスト。

```md
---
layout: image-left
image: https://example.com/photo.jpg
---
# タイトル
テキストコンテンツ
```

### two-cols

2カラム比較レイアウト。`::right::` で右カラムを分離。

```md
---
layout: two-cols
---
# 左カラム
- 項目A
- 項目B

::right::

# 右カラム
- 項目C
- 項目D
```

### cards

3カラムのカード型レイアウト。機能紹介やステップ説明に。
`::one::` `::two::` `::three::` で各カードの内容を定義。
Glass-morphism背景、グラデーション上部ボーダー付き。
ホバー時にグロー付きシャドウ＋浮き上がりアニメーション。

```md
---
layout: cards
---
# 見出し

::one::
### カード1タイトル
カード1の説明文

::two::
### カード2タイトル
カード2の説明文

::three::
### カード3タイトル
カード3の説明文
```

### comparison

ラベル付きの Before/After 比較レイアウト。`labelLeft` `labelRight` でラベルを指定。
中央にテーマカラーのディバイダーが入る。`::header::` で見出し、`::right::` で右カラムを定義。

```md
---
layout: comparison
labelLeft: Before
labelRight: After
---

::header::
# タイトル

::default::
変更前の内容

::right::
変更後の内容
```

### profile

自己紹介・人物紹介用。`image` propでアバター画像を丸枠で表示。
`::name::` で名前・肩書き、デフォルトスロットでプロフィール本文。

```md
---
layout: profile
image: https://example.com/avatar.jpg
---

::name::
# 名前
役職 / 所属

::default::
- 自己紹介の内容
- スキルや経験
```

### four-cards

2x2 グリッドのカードレイアウト。特徴や機能の一覧に。
`::header::` で見出し、`::one::` 〜 `::four::` で各セルを定義。
Glass-morphism背景、グラデーション上部ボーダー付き。
ホバー時にグロー付きシャドウ＋浮き上がりアニメーション。

```md
---
layout: four-cards
---

::header::
# タイトル

::one::
### ⚡ 高速
説明文

::two::
### 📝 簡単
説明文

::three::
### 🎨 美しい
説明文

::four::
### 🧩 拡張性
説明文
```

### timeline

3ステップのタイムライン。水平コネクターライン上にナンバー付き円（01, 02, 03）が並ぶ。
各ステップはGlass-morphismカード。`::header::` で見出し、`::one::` `::two::` `::three::` で各ステップの内容を定義。

```md
---
layout: timeline
---

::header::
## プロセス

::one::
### ステップ1
説明文

::two::
### ステップ2
説明文

::three::
### ステップ3
説明文
```

### highlight

左に大きな数値やメッセージ（グラデーション文字色）、右に補足情報を配置。
デフォルトスロットが左側、`::aside::` が右側パネル。

```md
---
layout: highlight
---
# 99.9%
稼働率

::aside::
### 高い信頼性
補足説明テキスト
```

### default

装飾なしの標準レイアウト。通常のスライドに使用。

---

## 独自スタイルクラス

Markdown 内で `<div class="クラス名">` として使える独自クラス。

### `.check` - チェックボックス

テーマカラーの枠線付きボックス。左上に「Check」ラベルが自動表示される。

```md
<div class="check">

確認してほしい内容をここに書く

</div>
```

### `.tips` - ヒント

強調枠線付きボックス。左上に「Tips」ラベルが自動表示される。テキストは小さめ。

```md
<div class="tips">

補足情報やヒントをここに書く

</div>
```

### `.quotation` - 引用元

右寄せで表示。先頭に「引用元:」が自動付与される。

```md
<div class="quotation">

書籍名 / 著者名

</div>
```

### `.copyright` - コピーライト

右寄せの極小テキスト。

```md
<div class="copyright">© 2026 shio3ch</div>
```

### `.extra` - 補足

上下マージン付きのミュートカラーテキスト。

```md
<div class="extra">

補足的な情報

</div>
```

---

## デザイン特徴

- **カラー**: エメラルドグリーン基調（`#10b981`）
- **フォント**: [M PLUS 2](https://fonts.google.com/specimen/M+PLUS+2)（日本語対応）
- **見出し装飾**: h1〜h3 に手書き風の波線アンダーライン
- **カード装飾**: Glass-morphism背景、自動ナンバリング、グラデーション上部ボーダー、ホバーでグロー付きシャドウ
- **グラデーション**: エメラルドグリーン→ティールのグラデーションアクセント
- **シャドウ**: sm/md/lg の3段階シャドウ + グローエフェクト
- **テーブル**: テーマカラーのヘッダー、交互背景色
- **リスト**: ネストに応じてマーカーが変化（●→○→■）
- **ダーク/ライト**: 両モード完全対応
- **マスコット**: 右下にカッパが表示（一部レイアウトでは非表示）
