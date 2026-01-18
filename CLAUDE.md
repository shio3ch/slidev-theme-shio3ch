# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト概要

Slidev用のカスタムテーマ（slidev-theme-shio3ch）。Denoを使用してSlidevを実行する構成。

## 開発コマンド

```sh
# 開発サーバー起動
deno task dev

# ビルド
deno task build

# PDFエクスポート
deno task export
```

## アーキテクチャ

```
theme/                    # テーマ本体
├── layouts/              # スライドレイアウト（Vue SFC）
│   ├── default.vue       # デフォルトレイアウト
│   └── cover.vue         # カバーレイアウト
├── styles/index.css      # テーマのCSS（CSS変数でカラー定義）
├── setup/main.ts         # テーマ初期化・スタイル読み込み
└── package.json          # テーマメタデータ

slides.md                 # プレビュー用サンプルスライド
```

## テーマ開発のポイント

- 新しいレイアウトを追加する場合は `theme/layouts/` にVueファイルを作成
- カラーやスタイルの変更は `theme/styles/index.css` のCSS変数を編集
- `slides.md` でテーマの見た目を確認しながら開発
