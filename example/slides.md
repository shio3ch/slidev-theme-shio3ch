---
theme: ..
layout: cover
---

# Presentation title

Presentation subtitle

---

# Slide Title

Slide Subtitle

- Slide bullet text
  - Slide bullet text
  - Slide bullet text
- Slide bullet text
- Slide bullet text

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Slide Title

Colons can be used to align columns.

| Tables        |      Are      |  Cool |
| ------------- | :-----------: | ----: |
| col 3 is      | right-aligned | $1600 |
| col 2 is      |   centered    |   $12 |
| zebra stripes |   are neat    |    $1 |

---
layout: section
---

# section layout

---
layout: statement
---

# statement layout

---
layout: fact
---

# fact layout

Fact information

---
layout: quote
---

## quote layout

Attribution

---
layout: image-left
image: public/profile.png
---

# image-left layout

---
layout: two-cols
---

::header::

# two-cols layout

育三

::left::

## ::left::

- 左側のコンテンツ
- テキストや図を配置
- 対比して見せたい時に

::right::

## ::right::

- 右側のコンテンツ
- こちらにも自由に配置
- Before / After にも

---
layout: cards
---

# cards layout

::one::

### 高速

Slidevはブラウザベースで高速なプレゼンテーションを実現します。

::two::

### 柔軟

Markdownで書けて、Vueコンポーネントも使えます。

::three::

### 美しい

テーマによるカスタマイズで美しいスライドを作成できます。

---
layout: comparison
labelLeft: Before
labelRight: After
---

::header::

# Comparison Layout

::default::

```ts
function calc(a, b, c) {
  return a * b + c - a;
}
```

- 変数名が不明瞭
- 処理の意図がわからない

::right::

```ts
function calculateTotal(price: number, quantity: number, tax: number) {
  return price * quantity + tax - price;
}
```

- 型付きで安全
- 意味のある命名

---
layout: profile
image: public/profile.png
---

::name::

# ロビンソン

森の妖精

::default::

- きゅうりそんなに好きじゃない

---
layout: four-cards
---

::header::

## four-cards layout

::one::

### ⚡ 高速

ブラウザベースでホットリロード対応。書いたらすぐ反映。

::two::

### 📝 Markdown

慣れた Markdown で書ける。コードブロックもそのまま。

::three::

### 🎨 テーマ

テーマを切り替えるだけでデザインが変わる。

::four::

### 🧩 拡張性

Vue コンポーネントで自由にカスタマイズ可能。

---

# Code

```ts {all|2|1-6|all}
interface User {
  id: number;
  firstName: string;
  lastName: string;
  role: string;
}

function updateUser(id: number, update: Partial<User>) {
  const user = getUser(id);
  const newUser = { ...user, ...update };
  saveUser(id, newUser);
}
```

---
layout: center
class: "text-center"
---

# Learn More

[Documentations](https://sli.dev) / [GitHub Repo](https://github.com/slidevjs/slidev)
