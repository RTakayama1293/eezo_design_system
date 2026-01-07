# EEZO Design System

北海道食材ECサイト「EEZO」のShopify移行に伴うデザインシステム構築プロジェクト。

## 概要

| 項目 | 内容 |
|------|------|
| プロジェクト名 | EEZO Design System |
| 目的 | Shopify移行時のUI/UX統一基盤構築 |
| ブランドコンセプト | 「現代の北前船」 |
| 実装担当 | 松永さん（エディ） |

## ディレクトリ構成

```
eezo-design-system/
├── CLAUDE.md                    # Claude Code用指示書（最重要）
├── README.md                    # 本ファイル
├── .claude/
│   └── settings.json            # フック設定
│
├── reference/                   # 参考資料（編集禁止）
│   ├── current_site/            # 現状EEZOのスクショ
│   ├── inspiration/             # 参考サイトのスクショ
│   └── brand_assets/            # 既存ロゴ等
│
├── outputs/                     # 生成物
│   ├── design_system/           # デザインシステム
│   │   ├── colors.html
│   │   ├── typography.html
│   │   └── design_tokens.css
│   │
│   ├── components/              # UIコンポーネント
│   │   ├── buttons.html
│   │   ├── cards.html
│   │   ├── forms.html
│   │   ├── navigation.html
│   │   └── banners.html
│   │
│   ├── pages/                   # ページテンプレート
│   │   ├── top.html
│   │   ├── product_list.html
│   │   ├── product_detail.html
│   │   └── cart.html
│   │
│   └── assets/                  # アセット
│       └── icons/
│
└── docs/                        # ドキュメント
    └── usage_guide.md
```

## 使い方

### 1. Claude Code on the Web でセッション開始

1. https://claude.ai/code にアクセス
2. 本リポジトリを選択
3. セッション開始

### 2. デザインシステム生成を依頼

```
CLAUDE.md を読んで、デザインシステムを構築して
```

または段階的に：

```
Phase 1: design_tokens.css とカラーパレット一覧を作成して
```

```
Phase 2: ボタンと商品カードのコンポーネントを作成して
```

### 3. 成果物の確認

PRを作成してGitHubにマージ後、`outputs/` 配下を確認。

## ブランドカラー（クイックリファレンス）

| 名前 | HEX | 用途 |
|------|-----|------|
| Navy | #1a2a3a | メイン |
| Gold | #c9a962 | アクセント |
| Cream | #f8f5ef | 背景 |

## 関連リンク

- [EEZOサイト](https://eezo.club/)
- [Shopify Theme Documentation](https://shopify.dev/themes)
- [新日本海商事](内部リンク)

---

*Created: 2026-01-07*
