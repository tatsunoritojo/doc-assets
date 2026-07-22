# デバイス枠・背景の使い方

パス基準: `~/Github/doc-assets/frames/`

| ファイル | 用途 |
|----------|------|
| `browser.svg` | プレースホルダ付きブラウザ（単体プレビュー） |
| `browser-mask.svg` | **重ね用**（画面部分が穴） |
| `phone.svg` / `phone-mask.svg` | 縦スマホ |
| `tablet.svg` / `tablet-mask.svg` | 横タブレット |
| `card.svg` | 汎用カード枠 |
| `bg-light.svg` / `bg-dark.svg` | 下敷き |

## HTML 合成（推奨）

スクリーンショットの上に mask 枠を重ねる。

```html
<!-- ブラウザ -->
<div style="position:relative; max-width:720px; margin:0 auto;">
  <img src="./shot-desktop.png" alt=""
       style="position:absolute; left:1.25%; top:8.1%; width:97.5%; height:90%;
              object-fit:cover; border-radius:6px; z-index:0;" />
  <img src="/Users/tatsu/Github/doc-assets/frames/browser-mask.svg" alt=""
       style="position:relative; width:100%; z-index:1; pointer-events:none;" />
</div>
```

```html
<!-- スマホ -->
<div style="position:relative; width:280px; margin:0 auto;">
  <img src="./shot-mobile.png" alt=""
       style="position:absolute; left:4.6%; top:7.5%; width:90.8%; height:85%;
              object-fit:cover; border-radius:28px; z-index:0;" />
  <img src="/Users/tatsu/Github/doc-assets/frames/phone-mask.svg" alt=""
       style="position:relative; width:100%; z-index:1; pointer-events:none;" />
</div>
```

比率は viewBox から:

| 枠 | 画面のおおよそ位置 |
|----|-------------------|
| browser | left 1.25% · top 8.1% · w 97.5% · h 90% |
| phone | left 4.6% · top 7.5% · w 90.8% · h 85% |
| tablet | left 2.7% · top 3.9% · w 94.5% · h 92.2% |

## Markdown 単体

枠だけ見せる（中は "screenshot" プレースホルダ）:

```markdown
![Browser](/Users/tatsu/Github/doc-assets/frames/browser.svg)
![Phone](/Users/tatsu/Github/doc-assets/frames/phone.svg)
```

GitHub README では HTML 重ねが効かないことが多い → **合成済み PNG を書き出してから**貼る。

## 合成 PNG の作り方（手元）

1. Playwright / ブラウザでスクショ取得  
2. 上記 HTML をローカルで開く、または `sips` / Figma で重ねる  
3. `docs/assets/` に `yymmdd_*.png` で保存  

## 背景板

```html
<div style="position:relative; padding:48px; background:#0F172A;">
  <img src="/Users/tatsu/Github/doc-assets/frames/bg-dark.svg"
       style="position:absolute; inset:0; width:100%; height:100%; object-fit:cover; opacity:.9;" alt="" />
  <div style="position:relative; z-index:1;">
    <!-- icons or frame here -->
  </div>
</div>
```

プレビュー: [preview-frames.html](../preview-frames.html)
