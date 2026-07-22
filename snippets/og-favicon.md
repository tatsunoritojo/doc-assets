# OGP / favicon

## サイズ

| 用途 | 推奨 |
|------|------|
| Open Graph / Twitter card | **1200×630** |
| favicon タブ | 16 / 32（SVG 可） |
| Apple touch | 180×180 |
| PWA maskable | 安全領域を中央に（`maskable.svg`） |

## OGP テンプレ

| ファイル | 用途 |
|----------|------|
| `og/1200x630_light.svg` | ライト + タイトル位置ガイド |
| `og/1200x630_dark.svg` | ダーク + ガイド |
| `og/1200x630_accent.svg` | アクセント（左バー）+ ガイド |
| `og/*_clean.svg` | **書き出し用**（ガイドなし） |

### 使い方

1. `*_clean.svg` をベースに、タイトルを Figma / ブラウザ / ImageMagick で載せる  
2. PNG で書き出し（SNS は PNG/JPEG が無難）  
3. プロジェクトの `public/og.png` 等へ  

ガイド付き版は**レイアウト検討用**。本番 URL には clean から作った PNG を使う。

```html
<meta property="og:image" content="https://example.com/og.png" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
<meta name="twitter:card" content="summary_large_image" />
```

### A+C との関係

- 背景は静かな板。偽 UI や架空ダッシュボードは描かない  
- プロダクト画面を載せたいなら**実スクショ**を中央に載せる  

## favicon

| ファイル | 用途 |
|----------|------|
| `favicon/icon.svg` | ベース（差し替え前提の抽象マーク） |
| `favicon/icon-16.svg` / `icon-32.svg` | 固定サイズ |
| `favicon/icon-dark.svg` | ダーク UI 向け |
| `favicon/apple-touch-180.svg` | iOS ホーム |
| `favicon/maskable.svg` | PWA 用ソリッド |

```html
<link rel="icon" href="/favicon.svg" type="image/svg+xml" />
<link rel="apple-touch-icon" href="/apple-touch-icon.png" />
```

**マークは汎用の抽象形**。案件の正式ロゴがある場合は `icon.svg` を差し替える。

### SVG → PNG（任意）

```bash
# rsvg-convert や qlmanage 等、環境にあるツールで
# 例: 180px
# rsvg-convert -w 180 -h 180 apple-touch-180.svg -o apple-touch-icon.png
```

プレビュー: [preview-og.html](../preview-og.html)
