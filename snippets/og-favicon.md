# OGP / favicon

## いつ使うか

公開 URL を X / Slack / Discord / LINE 等に**貼ったときのプレビュー画像**。  
非公開だけのリポでは不要。portfolio・LP・ブログ・デモ URL 向け。

## サイズ

| 用途 | 推奨 |
|------|------|
| Open Graph / X large card | **1200×630** |
| favicon | 16 / 32（SVG 可） |
| Apple touch | 180×180 |
| PWA maskable | `favicon/maskable.svg` |

---

## OGP テンプレ一覧（`og/`）

命名: `1200x630_<用途>.svg` = レイアウト検討（ガイド付き）  
`1200x630_<用途>_clean.svg` = **本番書き出し用**（ガイドなし）

### 用途別

| 用途 | guide | clean | 向いている場面 |
|------|-------|-------|----------------|
| light / dark / accent | 既存 | 既存 | 汎用 |
| **blog** | `..._blog.svg` | `..._blog_clean.svg` | 記事・writings |
| **product** | `..._product.svg` | `..._product_clean.svg` | SaaS / 左コピー右スクショ |
| **product_light** | `..._product_light.svg` | `..._product_light_clean.svg` | 同上・明るい版 |
| **portfolio** | `..._portfolio.svg` | `..._portfolio_clean.svg` | 個人サイト・中央タイトル |
| **minimal** | `..._minimal.svg` | `..._minimal_clean.svg` | 余白最大・白 |
| **minimal_dark** | `..._minimal_dark.svg` | `..._minimal_dark_clean.svg` | 余白最大・黒 |
| **announce** | `..._announce.svg` | `..._announce_clean.svg` | リリース・告知 |
| **split_v** | `..._split_v.svg` | `..._split_v_clean.svg` | 上画像・下タイトル |
| **docs** | `..._docs.svg` | `..._docs_clean.svg` | 技術ドキュメント・README 公開 |
| **warm** | `..._warm.svg` | `..._warm_clean.svg` | やわらかいトーン |

### 選び方（ざっくり）

```
記事を貼る          → blog / split_v
プロダクト URL      → product（スクショあり）or announce
ポートフォリオ      → portfolio / minimal
社内に近い・静か    → minimal / docs
個人・教育っぽさ    → warm
```

### 作り方

1. 用途の **`_clean.svg`** を開く  
2. タイトル（必要なら**実スクショ**）を載せる  
3. PNG 1200×630 で書き出し → `public/og.png` 等  

guide 版は配置の当たり用。本番 meta には clean から作った PNG を使う。

```html
<meta property="og:image" content="https://example.com/og.png" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
<meta name="twitter:card" content="summary_large_image" />
```

### A+C

- 偽ダッシュボードは描かない  
- 画面が要るなら実スクショを slot に載せる（product / split_v）

---

## favicon（変更なし）

| ファイル | 用途 |
|----------|------|
| `favicon/icon.svg` | ベース（案件ロゴで差し替え可） |
| `icon-16.svg` / `icon-32.svg` | 固定サイズ |
| `icon-dark.svg` | ダーク向け |
| `apple-touch-180.svg` | iOS |
| `maskable.svg` | PWA |

```html
<link rel="icon" href="/favicon.svg" type="image/svg+xml" />
<link rel="apple-touch-icon" href="/apple-touch-icon.png" />
```

プレビュー: [preview-og.html](../preview-og.html)
