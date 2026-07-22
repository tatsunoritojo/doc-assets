# doc-assets

README・サービスフロー図・提案資料向けの**ドキュメント用アセットキット**。

アイコンを探す時間を減らし、図とバッジの見た目を揃えるためのローカル素材集です。

## 何が入っているか

| 領域 | パス | 内容 |
|------|------|------|
| ブランド | `icons/brands/` | カラーロゴ（本線） |
| 単色ブランド | `icons/brands-mono/` | 地色に溶かす用 |
| 汎用記号 | `icons/{actors,flow,status,data,infra,ui}/` | Lucide 線画 |
| バッジ | `badges/static/` | 静的 SVG バッジ |
| フロー雛形 | `templates/flows/` | Mermaid テンプレ |
| 色 | `tokens/` | Mermaid classDef / colors |
| デバイス枠 | `frames/` | browser / phone / tablet + mask |
| GUI 記号 | `windows/` `chrome/` `cursors/` | **ワイヤのみ**（A+C） |
| OGP / favicon | `og/` `favicon/` | 1200×630 型紙・favicon 雛形 |
| スニペット | `snippets/` | コピペ用 Markdown/HTML |
| プレビュー | `preview-*.html` | ブラウザで一覧 |

**画面の中身は実スクショが正。** 手描きの色付き UI で本物のフリをしない（旧モックは `archive/`）。

## すぐ使う

```bash
git clone https://github.com/<you>/doc-assets.git
cd doc-assets
open preview-brands.html   # またはブラウザで開く
```

```markdown
![Vercel](icons/brands/vercel.svg)
![Sheets](icons/brands/googlesheets.svg)
![build](badges/static/build-passing.svg)
```

プロジェクトへ取り込む:

```bash
cp -R icons ./docs/assets/icons
cp -R badges/static ./docs/assets/badges
```

## プレビュー

| ファイル | 内容 |
|----------|------|
| [preview-brands.html](./preview-brands.html) | ブランドアイコン |
| [preview-badges.html](./preview-badges.html) | 静的バッジ |
| [preview-tools.html](./preview-tools.html) | ツール系アイコン |
| [preview-frames.html](./preview-frames.html) | デバイス枠 |
| [preview-gui.html](./preview-gui.html) | ワイヤ GUI + カーソル |
| [preview-og.html](./preview-og.html) | OGP テンプレ |

## ドキュメント

| ファイル | 内容 |
|----------|------|
| [catalog.md](./catalog.md) | アセット索引 |
| [LICENSES.md](./LICENSES.md) | 第三者ライセンス |
| [docs/tools-by-category.md](./docs/tools-by-category.md) | ツール → アイコン名 |
| [docs/brand-selection.md](./docs/brand-selection.md) | ブランド選定の考え方 |
| [snippets/](./snippets/) | badges / frames / OGP / GUI など |

## GUI 方針（A+C）

1. 画面は**実スクショ**  
2. `frames/*-mask` でデバイス枠  
3. `cursors/*` で操作位置  
4. `windows/` `chrome/` は**線画記号**のみ  

詳細: [snippets/gui-chrome.md](./snippets/gui-chrome.md)

## OGP

公開 URL を SNS に貼るときの 1200×630 背景。  
`og/*_clean.svg` にタイトル（必要ならスクショ）を載せて PNG 化。  

→ [snippets/og-favicon.md](./snippets/og-favicon.md)

## 出典

- **Lucide** — ISC（汎用アイコン）  
- **Simple Icons** — CC0（ブランド形状）。色は brand hex を fill  
- 図解用カスタム（Grok / xAI 等）— 記号用。公式ではない  
- 詳細: [LICENSES.md](./LICENSES.md)

ブランドの商標は各社に帰属します。公開資料では各ガイドラインに従ってください。

## 追加方針

- 足りないブランド・ワイヤは**都度追加**  
- 色付き「偽 UI」モックは本線に戻さない  

## ライセンス

キット独自の文書・構成・ワイヤ SVG は [MIT](./LICENSE)（第三者アイコンは上記の各ライセンスが優先）。
