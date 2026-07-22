# doc-assets

README・サービスフロー図・設計メモ向けの**横断アイコンキット**。

- **本線はカラーブランド**（`icons/brands/`）
- 単色控えは `icons/brands-mono/`
- フロー記号（人・矢印・状態）は Lucide 線画（単色）のまま

`.private-ai-assets`（生成画像）とは別物。

## Phase 1 追加（2026-07-23）

| パス | 内容 |
|------|------|
| `badges/static/` | 静的 badge SVG 40 |
| `snippets/badges.md` | Shields 動的 + 静的の貼り方・リポ別プリセット |
| `templates/flows/` | サービスフロー雛形 10 |
| `tokens/mermaid.md` | Mermaid classDef 共通 |
| `tokens/colors.json` | 色トークン |

### 最短ルート

1. バッジ: [snippets/badges.md](./snippets/badges.md)
2. フロー図: [templates/flows/](./templates/flows/)
3. 色揃え: [tokens/mermaid.md](./tokens/mermaid.md)
4. ブランド: [preview-brands.html](./preview-brands.html)


## 置き場所

```
~/Github/doc-assets/
```

ブラウザで一覧: [preview-brands.html](./preview-brands.html)（Finder から開く）

## ディレクトリ

| パス | 用途 |
|------|------|
| **`icons/brands/`** | **本線・カラー**（公式 brand color / 多色 Google 等） |
| `icons/brands-mono/` | 単色 SVG（図の地色に溶かす用） |
| `icons/actors/` | 人・端末・組織（Lucide・単色） |
| `icons/flow/` | 矢印・分岐・ループ |
| `icons/status/` | 成功・失敗・警告・loading |
| `icons/data/` | DB・ファイル・webhook |
| `icons/infra/` | サーバ・鍵・ネットワーク |
| `icons/ui/` | 検索・設定・メール・QR |
| `snippets/` | Markdown / Mermaid 雛形 |

全件: [catalog.md](./catalog.md) · ライセンス: [LICENSES.md](./LICENSES.md) · 観測: [docs/service-inventory.md](./docs/service-inventory.md)

## AI / エージェント（分離済み）

| 名前 | パス | 備考 |
|------|------|------|
| Claude（星） | `icons/brands/claude.svg` | Simple Icons の starburst。**Anthropic とは別** |
| Anthropic（A字） | `icons/brands/anthropic.svg` | 社名マーク |
| Claude Code | `icons/brands/claudecode.svg` | Claude 星の色違い |
| OpenAI | `icons/brands/openai.svg` | 紫 |
| ChatGPT | `icons/brands/chatgpt.svg` | 緑（同一マーク・色で区別） |
| Codex | `icons/brands/codex.svg` | 黒寄り（同一マーク・色で区別） |
| Grok | `icons/brands/grok.svg` | 図解用カスタム（公式 SI なし） |
| xAI | `icons/brands/xai.svg` | 図解用カスタム |
| Gemini | `icons/brands/gemini.svg` / `googlegemini.svg` | |

## よく使うカラーブランド

| 用途 | パス |
|------|------|
| Vercel | `icons/brands/vercel.svg` |
| GitHub | `icons/brands/github.svg` |
| Google（多色） | `icons/brands/google.svg` |
| Sheets / Drive / Calendar / GAS | `googlesheets` / `googledrive` / `googlecalendar` / `googleappsscript` |
| LINE | `icons/brands/line.svg` |
| Neon / PostgreSQL | `neon` / `postgresql` |
| Cloudflare | `icons/brands/cloudflare.svg` |
| Obsidian | `icons/brands/obsidian.svg` |
| X / Discord / Slack | `x` / `discord` / `slack` |
| Notion / Figma | `notion` / `figma` |
| Netlify / Firebase / Supabase | 各 `icons/brands/<name>.svg` |

## Markdown

```markdown
![Claude](/Users/tatsu/Github/doc-assets/icons/brands/claude.svg)
![ChatGPT](/Users/tatsu/Github/doc-assets/icons/brands/chatgpt.svg)
![Grok](/Users/tatsu/Github/doc-assets/icons/brands/grok.svg)
```

プロジェクトへ:

```bash
cp -R ~/Github/doc-assets/icons ./docs/assets/icons
```

## 方針

1. **brands = カラーが正**。白黒が欲しいときだけ mono
2. 実利用 + 周辺推測（AI・SNS・ナレッジ・ホスティング）を収録
3. Lucide 汎用は単色維持（図がうるさくならない）
4. 商標: 公開資料では各社ガイドラインに従う。Grok/xAI は SI 非掲載のため**図解用簡易マーク**

## 未収録・代替

| 欲しい名前 | 状態 |
|------------|------|
| Playwright | `icons/ui/test.svg` |
| Fanvue 等一部 | SI に無し |
| Grok / xAI 公式 | カスタム図解マーク（差し替え歓迎） |
