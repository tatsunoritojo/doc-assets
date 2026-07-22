# GUI 支援アセット（window / cursor / chrome）

| ディレクトリ | 用途 |
|--------------|------|
| `windows/` | ダイアログ・パネル・アプリ枠・トースト |
| `cursors/` | マウスカーソル（図解用 SVG） |
| `chrome/` | ボタン・入力・tooltip・focus・toggle 等 |

## カーソルを「操作中」に見せる

```html
<div style="position:relative; display:inline-block;">
  <img src="/Users/tatsu/Github/doc-assets/frames/browser.svg" width="480" alt="" />
  <img src="/Users/tatsu/Github/doc-assets/cursors/pointer.svg"
       width="28" height="28" alt=""
       style="position:absolute; left:62%; top:48%; filter:drop-shadow(0 1px 1px rgba(0,0,0,.35));" />
</div>
```

| カーソル | ファイル | 使う場面 |
|----------|----------|----------|
| 矢印 | `cursors/default.svg` | 通常 |
| 指 | `cursors/pointer.svg` | クリック可能 |
| I ビーム | `cursors/text.svg` | テキスト入力 |
| 移動 | `cursors/move.svg` | ドラッグ |
| 禁止 | `cursors/not-allowed.svg` | 無効 |
| 待ち | `cursors/wait.svg` | 処理中 |
| 十字 | `cursors/crosshair.svg` | 精密選択 |
| つかむ | `cursors/grab.svg` | パン |

## ウィンドウ部品

```markdown
![Dialog](/Users/tatsu/Github/doc-assets/windows/dialog.svg)
![Modal](/Users/tatsu/Github/doc-assets/windows/modal-backdrop.svg)
![App](/Users/tatsu/Github/doc-assets/windows/window-app.svg)
![Toast](/Users/tatsu/Github/doc-assets/windows/toast.svg)
```

| ファイル | 用途 |
|----------|------|
| `dialog.svg` | 確認ダイアログ |
| `modal-backdrop.svg` | 背面暗転 + 中央ダイアログ |
| `panel.svg` | サイドパネル |
| `menubar.svg` | メニューバー |
| `dropdown.svg` | ドロップダウン |
| `window-app.svg` | サイドバー付きアプリ窓 |
| `toast.svg` | 保存完了などのトースト |

## UI コントロール

```markdown
![Primary](/Users/tatsu/Github/doc-assets/chrome/button-primary.svg)
![Focus](/Users/tatsu/Github/doc-assets/chrome/focus-ring.svg)
![Tooltip](/Users/tatsu/Github/doc-assets/chrome/tooltip.svg)
```

フロー図の横に「この画面でポインタはここ」と添える用途向け。本番 UI の代替ではない。

プレビュー: [preview-gui.html](../preview-gui.html)
