# GUI 記号（A+C 方針）

## 原則

1. **画面の中身は実スクショが正**（手描き UI で本物のフリをしない）
2. **window / chrome はワイヤ記号**（線のみ・色なし・英語ラベルなし）
3. **カーソルは注釈用**（どの操作かを示す）
4. 色付き旧モックは `archive/gui-filled-20260723/`（本線で使わない）

## 推奨レイヤ

```
[背景 bg 任意]
  └ [実スクショ]
      └ [frames/*-mask.svg  デバイス枠]
          └ [cursors/*.svg  ポインタ注釈]
```

ダイアログの**中身**を描きたいときも、ワイヤ `windows/dialog.svg` は「箱の記号」だけ。文言やボタン色はスクショ側。

## カーソル注釈

```html
<div style="position:relative; display:inline-block; max-width:560px;">
  <img src="./shot.png" alt="画面" style="width:100%; display:block; border-radius:8px;" />
  <img src="/Users/tatsu/Github/doc-assets/cursors/pointer.svg"
       width="28" height="28" alt=""
       style="position:absolute; left:58%; top:42%;
              filter:drop-shadow(0 1px 1px rgba(0,0,0,.35)); pointer-events:none;" />
</div>
```

| ファイル | 用途 |
|----------|------|
| `cursors/default.svg` | 通常 |
| `cursors/pointer.svg` | クリック |
| `cursors/text.svg` | 入力 |
| `cursors/move.svg` | 移動 |
| `cursors/not-allowed.svg` | 不可 |
| `cursors/wait.svg` | 待ち |
| `cursors/crosshair.svg` | 精密 |
| `cursors/grab.svg` | パン |

## ワイヤ記号（状態・構造の説明）

```markdown
![dialog](/Users/tatsu/Github/doc-assets/windows/dialog.svg)
![modal](/Users/tatsu/Github/doc-assets/windows/modal.svg)
![app](/Users/tatsu/Github/doc-assets/windows/window-app.svg)
![button](/Users/tatsu/Github/doc-assets/chrome/button.svg)
![focus](/Users/tatsu/Github/doc-assets/chrome/focus.svg)
```

フロー図のノード横に「ここでモーダル」と添える程度に使う。

## やらないこと

- 色付き OK ボタンの手描きを README ヒーローに載せる  
- `Dialog title` / `Button` 英語プレースホルダの復活  
- 旧 `archive/gui-filled-*` を本線に戻す  

プレビュー: [preview-gui.html](../preview-gui.html)
