# EEZO Design System - Assets

## ディレクトリ構成

```
assets/
├── icons/
│   └── icons.svg    # SVGスプライトアイコン
└── readme.md        # このファイル
```

## アイコンの使用方法

### SVGスプライト方式（推奨）

`icons/icons.svg` はSVGスプライト形式で提供されています。以下の方法で使用できます。

#### インラインSVG（推奨）

```html
<svg width="24" height="24" fill="currentColor">
  <use href="assets/icons/icons.svg#icon-cart"></use>
</svg>
```

#### CSS変数でサイズを制御

```css
.icon {
  width: 24px;
  height: 24px;
  fill: currentColor;
}

.icon--sm { width: 16px; height: 16px; }
.icon--md { width: 24px; height: 24px; }
.icon--lg { width: 32px; height: 32px; }
```

```html
<svg class="icon icon--lg">
  <use href="assets/icons/icons.svg#icon-heart"></use>
</svg>
```

### 利用可能なアイコン一覧

| アイコンID | 用途 |
|-----------|------|
| `icon-search` | 検索 |
| `icon-cart` | カート |
| `icon-heart` | お気に入り（塗りつぶし） |
| `icon-heart-outline` | お気に入り（アウトライン） |
| `icon-user` | ユーザー・アカウント |
| `icon-menu` | ハンバーガーメニュー |
| `icon-close` | 閉じる |
| `icon-chevron-left` | 左矢印 |
| `icon-chevron-right` | 右矢印 |
| `icon-chevron-down` | 下矢印 |
| `icon-chevron-up` | 上矢印 |
| `icon-arrow-left` | 戻る |
| `icon-arrow-right` | 進む |
| `icon-check` | チェックマーク |
| `icon-check-circle` | チェック（丸囲み） |
| `icon-error` | エラー・警告 |
| `icon-info` | 情報 |
| `icon-delete` | 削除 |
| `icon-edit` | 編集 |
| `icon-plus` | プラス |
| `icon-minus` | マイナス |
| `icon-lock` | セキュリティ・ロック |
| `icon-mail` | メール |
| `icon-phone` | 電話 |
| `icon-location` | 場所 |
| `icon-shipping` | 配送 |
| `icon-gift` | ギフト |
| `icon-star` | 星（塗りつぶし） |
| `icon-star-outline` | 星（アウトライン） |
| `icon-filter` | フィルター |
| `icon-grid` | グリッド表示 |
| `icon-list` | リスト表示 |
| `icon-share` | 共有 |
| `icon-instagram` | Instagram |
| `icon-facebook` | Facebook |
| `icon-twitter` | Twitter/X |
| `icon-line` | LINE |

## カラーの適用

アイコンは `fill: currentColor` を使用しているため、親要素の `color` プロパティを継承します。

```css
/* ボタン内のアイコン */
.btn svg {
  fill: currentColor;
}

/* 特定の色を指定する場合 */
.icon--gold {
  fill: var(--eezo-gold);
}

.icon--navy {
  fill: var(--eezo-navy);
}
```

## Shopify Liquidでの使用

Shopifyテーマでは、`snippets` ディレクトリにアイコン用のスニペットを作成することを推奨します。

### snippets/icon.liquid

```liquid
{% comment %}
  Usage: {% render 'icon', name: 'cart', size: 24 %}
{% endcomment %}

{% assign icon_size = size | default: 24 %}

<svg width="{{ icon_size }}" height="{{ icon_size }}" fill="currentColor" aria-hidden="true">
  <use href="{{ 'icons.svg' | asset_url }}#icon-{{ name }}"></use>
</svg>
```

### 使用例

```liquid
{% render 'icon', name: 'cart', size: 24 %}
{% render 'icon', name: 'heart', size: 20 %}
```

## アクセシビリティ

- 装飾目的のアイコンには `aria-hidden="true"` を付与
- 意味を持つアイコンには適切な `aria-label` を付与

```html
<!-- 装飾アイコン（ラベルがある場合） -->
<button>
  <svg aria-hidden="true">
    <use href="#icon-cart"></use>
  </svg>
  カートに入れる
</button>

<!-- 意味を持つアイコン（ラベルがない場合） -->
<button aria-label="カートを見る">
  <svg aria-hidden="true">
    <use href="#icon-cart"></use>
  </svg>
</button>
```

## 画像アセットについて

本デザインシステムには画像ファイルは含まれていません。
実装時には以下のガイドラインに従って画像を準備してください：

### 商品画像

| 用途 | 推奨サイズ | アスペクト比 |
|------|-----------|-------------|
| 一覧カード | 400x300px | 4:3 |
| 詳細メイン | 800x800px | 1:1 |
| 詳細サムネイル | 100x100px | 1:1 |
| カート内 | 120x120px | 1:1 |

### バナー画像

| 用途 | 推奨サイズ |
|------|-----------|
| ヒーロー | 1920x800px |
| プロモーション | 1200x600px |
| カテゴリー | 600x400px |

### 画像形式

- **写真**: WebP（フォールバック用にJPEG）
- **ロゴ・アイコン**: SVG
- **背景パターン**: SVGまたはCSS

### 画像の最適化

- 商品画像は必ず圧縮を行う
- レスポンシブ画像（srcset）の使用を推奨
- Lazy loadingを適用（loading="lazy"）

---

*EEZO Design System v1.0*
