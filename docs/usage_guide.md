# EEZO Design System 使用ガイド

本ドキュメントは、デザインシステム生成後に実装担当（エディ）が参照するガイドです。
Claude Codeで生成された後、具体的な使用方法を追記します。

## クイックスタート

### 1. CSS変数の読み込み

```html
<link rel="stylesheet" href="design_system/design_tokens.css">
```

### 2. Google Fonts の読み込み

```html
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@300;400;500;700&family=Noto+Serif+JP:wght@400;600&display=swap" rel="stylesheet">
```

### 3. コンポーネントの使用

各コンポーネントHTMLからクラス名・構造をコピーして使用。

---

## コンポーネント一覧

| コンポーネント | ファイル | 用途 |
|---------------|----------|------|
| ボタン | buttons.html | CTA、アクション |
| カード | cards.html | 商品一覧 |
| フォーム | forms.html | 入力、購入フロー |
| ナビゲーション | navigation.html | ヘッダー、メニュー |
| バナー | banners.html | プロモーション |

---

## Shopifyへの組み込み

### Liquidテンプレートへの適用

（生成後に詳細を追記）

### テーマカスタマイズ

（生成後に詳細を追記）

---

## FAQ

### Q: 色を変更したい場合は？

`design_tokens.css` の CSS変数を変更してください。

### Q: 新しいコンポーネントを追加したい場合は？

既存コンポーネントの構造を参考に、同じCSS変数・命名規則で作成してください。

---

*このドキュメントはデザインシステム生成後に更新されます*
