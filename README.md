# doc-assets

README・サービスフロー図・設計メモ向けの**横断アイコンキット**。  
「毎回アイコンを探す」をやめて、ここからパスを貼るだけにする。

`.private-ai-assets`（生成画像）とは別物。ここは**説明図用 SVG**。

## 置き場所

```
~/Github/doc-assets/
```

## ディレクトリ

| パス | 用途 |
|------|------|
| `icons/actors/` | 人・端末・組織（user / student / bot / monitor 等） |
| `icons/flow/` | 矢印・分岐・ループ・ハンドオフ |
| `icons/status/` | 成功・失敗・警告・loading・empty |
| `icons/data/` | DB・ファイル・Sheets 相当・webhook |
| `icons/infra/` | サーバ・鍵・ネットワーク・盾 |
| `icons/ui/` | 検索・設定・メール・QR・チャート |
| `icons/brands/` | 実利用サービス（調査 2026-07-23 ベース） |
| `snippets/` | Markdown / Mermaid の貼り方 |
| `badges/` / `frames/` | 枠のみ（未収録） |

全件一覧: [catalog.md](./catalog.md)  
ライセンス: [LICENSES.md](./LICENSES.md)  
観測メモ（どのリポで何を使っているか）: [docs/service-inventory.md](./docs/service-inventory.md)

## よく使う 20（優先）

| 用途 | パス |
|------|------|
| Vercel | `icons/brands/vercel.svg` |
| GitHub | `icons/brands/github.svg` |
| Google Sheets | `icons/brands/googlesheets.svg` |
| Google Calendar | `icons/brands/googlecalendar.svg` |
| Google Drive | `icons/brands/googledrive.svg` |
| GAS | `icons/brands/googleappsscript.svg` |
| Google | `icons/brands/google.svg` |
| LINE | `icons/brands/line.svg` |
| Neon | `icons/brands/neon.svg` |
| PostgreSQL | `icons/brands/postgresql.svg` |
| Anthropic / Claude | `icons/brands/anthropic.svg` / `claude.svg` |
| Python | `icons/brands/python.svg` |
| Next.js | `icons/brands/nextdotjs.svg` |
| Netlify | `icons/brands/netlify.svg` |
| Firebase | `icons/brands/firebase.svg` |
| Supabase | `icons/brands/supabase.svg` |
| ユーザー | `icons/actors/user.svg` |
| 矢印 | `icons/flow/arrow-right.svg` |
| OK / Error | `icons/status/check.svg` / `error.svg` |
| QR | `icons/ui/qr-code.svg` |

## Markdown への貼り方

相対パス（リポ内にコピーした場合）:

```markdown
![Vercel](./assets/icons/brands/vercel.svg)
```

絶対パス（ローカルメモ・Obsidian 等）:

```markdown
![Sheets](/Users/tatsu/Github/doc-assets/icons/brands/googlesheets.svg)
```

HTML（サイズ固定）:

```html
<img src="/Users/tatsu/Github/doc-assets/icons/brands/vercel.svg" alt="Vercel" width="24" height="24" />
```

詳細は `snippets/markdown-embed.md` / `snippets/mermaid-icons.md`。

## 方針

1. **加法のみ** — 足りないものは足す。既存 SVG の削除は明示依頼があるときだけ
2. **ブランドは実測ベース** — `docs/service-inventory.md` に無いものを増やしすぎない
3. **Lucide = 汎用 / Simple Icons = ブランド** — ライセンスは LICENSES.md
4. **onedrop 局所 logos** は `onedrop/assets/diagrams/logos/` に残る。横断正本は本リポ

## 未収録（Simple Icons に無かったもの）

| 欲しい名前 | 代替 |
|------------|------|
| Playwright | `icons/ui/test.svg`（Lucide） |
| OpenAI | `icons/actors/bot.svg` または文中表記 |
| AWS | 未収録（要時に追加） |

## 更新手順

1. Simple Icons の slug を確認 → `icons/brands/<slug>.svg` を raw から取得
2. Lucide は `icons/<category>/<name>.svg`
3. `catalog.md` を更新（または `python3 scripts/gen-catalog.py` があれば実行）
4. 新規サービスをリポで使い始めたら `docs/service-inventory.md` に 1 行
