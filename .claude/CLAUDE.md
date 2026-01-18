# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト概要

Slidev用のカスタムテーマ（slidev-theme-shio3ch）。Denoを使用してSlidevを実行する構成。

## 開発コマンド

```sh
# example/ディレクトリに移動してから実行
cd example

# 開発サーバー起動
deno task dev

# ビルド
deno task build

# PDFエクスポート
deno task export
```

## アーキテクチャ

```
/                         # テーマ本体（ルート）
├── layouts/              # スライドレイアウト（Vue SFC）
│   ├── cover.vue         # カバーレイアウト
│   ├── fact.vue
│   ├── intro.vue
│   ├── quote.vue
│   ├── section.vue
│   └── statement.vue
├── styles/               # テーマのCSS
├── components/           # Vueコンポーネント
├── public/               # 静的ファイル
├── global-bottom.vue     # グローバルボトムコンポーネント
└── package.json          # テーマメタデータ

example/                  # 開発用ディレクトリ
├── slides.md             # プレビュー用サンプルスライド
└── deno.json             # 開発タスク
```

## テーマ開発のポイント

- 新しいレイアウトを追加する場合は `layouts/` にVueファイルを作成
- カラーやスタイルの変更は `styles/` 内のCSSファイルを編集
- `example/slides.md` でテーマの見た目を確認しながら開発

## 他プロジェクトからの利用

他のSlidevプロジェクトからGitHub経由でテーマを利用可能：

```json
{
  "dependencies": {
    "slidev-theme-shio3ch": "github:shio3ch/slidev-theme-shio3ch"
  }
}
```
