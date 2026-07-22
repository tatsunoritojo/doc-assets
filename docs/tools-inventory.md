# ツール台帳（観測 2026-07-23）

**観測** = この Mac 上で `command -v` / `npm ls -g` / `brew list` で確認したもの。  
**推論** = リポ依存や運用ドキュメントから「使う想定」だが PATH 未確認。  
**アイコン** = `icons/brands/<name>.svg`（無ければ備考）。

観測日: 2026-07-23 · ホスト: 東城 macOS

---

## エージェント / AI CLI

| ツール | 観測 | パス or 根拠 | 用途（短く） | icon |
|--------|------|--------------|--------------|------|
| Claude Code (`claude`) | 観測 | `~/.local/bin/claude` | 実装・統括セッション | `claude` / `claudecode` |
| Codex (`codex`) | 観測 | `~/.local/bin/codex` + npm `@openai/codex` | 敵対レビュー・実装 | `codex` / `openai` |
| Grok CLI / Build | 推論 | セッション運用・スキル | 調査・実装 | `grok` / `xai` |
| Cursor | 推論 | ブランド・スキルに存在 | エディタ兼エージェント | `cursor` |
| GitHub Copilot | 推論 | 周辺ツールとして言及 | 補完 | `copilot` / `githubcopilot` |
| Ollama | 観測 | `/usr/local/bin/ollama` | ローカル LLM | `ollama` |
| Gemini CLI | 未検出 | PATH に無し | — | `gemini` |

## デプロイ / クラウド CLI

| ツール | 観測 | パス or 根拠 | 用途 | icon |
|--------|------|--------------|------|------|
| Vercel CLI | 観測 | `~/.local/bin/vercel` + npm g | shifree / Next 系デプロイ | `vercel` |
| clasp | 観測 | `~/.local/bin/clasp` + npm `@google/clasp` | GAS push/pull | `googleappsscript` |
| gcloud | 観測 | Google Cloud SDK | CF / Secret Manager | `googlecloud` |
| Netlify CLI | 観測 | npm g `netlify-cli` | correspondence-school-finder 等 | `netlify` |
| Firebase tools | 観測 | npm g `firebase-tools` | habit-tracker 系 | `firebase` |
| EAS CLI | 観測 | npm g `eas-cli` | Expo ビルド | `expo` |
| gh | 観測 | `~/.local/bin/gh` | GitHub PR/Issue | `github` |
| Docker | 未検出 | PATH に無し（kintai 等では想定） | コンテナ | `docker` |

## 言語ランタイム / パッケージ

| ツール | 観測 | 用途 | icon |
|--------|------|------|------|
| git | 観測 `/usr/bin/git` | 版管理 | `git` |
| node / npm / npx | 観測 `~/.local/bin` | JS エコシステム | `nodedotjs` / `npm` |
| python3 / pip3 | 観測 `/usr/bin` | Flask / スクリプト | `python` |
| java | 観測 | 過去 kintai / 学習 | `java` |
| swift | 観測 | MacConcierge / iOS PoC | `swift` |
| ruby | 観測 | システム付属 | `ruby` |
| Homebrew | 観測 `/opt/homebrew` | パッケージ | `homebrew` |
| pnpm / yarn / bun | 未検出 | リポによっては packageManager | `pnpm` / `yarn` / `bun` |
| go / rustc / cargo | 未検出 | — | `go` / `rust` |

## 検証 / 品質

| ツール | 観測 | 根拠 | 用途 | icon |
|--------|------|------|------|------|
| Playwright | 未検出(CLI) | shifree / code-concierge / onedrop 依存 | E2E | `playwright` |
| pytest | 未検出(PATH) | shifree requirements | Python テスト | `pytest` |
| vitest | 推論 | code-concierge package.json | 単体 | `vitest` |
| eslint | 推論 | 各 Next リポ | lint | `eslint` |
| prettier | 推論 | code-concierge 等 | format | `prettier` |
| GitHub Actions | 推論 | `.github/workflows` | CI | `githubactions` |

## DB / データ

| ツール | 観測 | 用途 | icon |
|--------|------|------|------|
| sqlite3 | 観測 | ローカル DB | `sqlite` |
| psql | 未検出 | Neon 接続は URL + スクリプト想定 | `postgresql` / `neon` |
| Google Sheets (gspread) | 推論 | onedrop desktop | `googlesheets` |

## メディア / その他 CLI

| ツール | 観測 | 用途 | icon |
|--------|------|------|------|
| ffmpeg | 観測 brew | 動画処理 | `ffmpeg` |
| jq | 観測 | JSON | —（汎用 `terminal`） |
| fd / bat | 観測 | 検索・表示 | — |
| d2 | 観測 brew formula | 図（d2lang） | 未収録 |
| tree | 観測 brew | ディレクトリ | — |

## ナレッジ / コラボ（アプリ）

| ツール | 観測 | 用途 | icon |
|--------|------|------|------|
| Obsidian | 推論（Vault パス常用） | 第2の脳 | `obsidian` |
| Notion | 案件言及 | 失注含む周辺 | `notion` |
| Figma | 案件・デザイン | UI | `figma` |
| Slack / LINE / Discord | 運用 | 通知・Bot | 各 brand |

## エディタ / IDE（観測弱・周辺）

| ツール | 観測 | icon |
|--------|------|------|
| VS Code | 未検出 `code` | `visualstudiocode` |
| Xcode | 推論（swift あり） | `xcode` |
| JetBrains / PyCharm | 未検出 | `jetbrains` / `pycharm` |
| Warp / iTerm / Raycast | アイコンのみ収録 | 各 brand |

---

## 観測サマリ

| 区分 | 件数感 |
|------|--------|
| PATH で OK | git, gh, node, npm, npx, python3, brew, clasp, vercel, gcloud, java, swift, ruby, sqlite3, ollama, codex, claude, ffmpeg, jq, fd, bat, npm-globals… |
| リポ依存だが CLI 未確認 | Playwright, pytest, eslint, tsc, docker, psql |
| アイコン brands 数 | 補完後 200+（catalog 参照） |

**推論で断定しない:** 「Docker は使っていない」ではなく「PATH に無い」。CI や他マシンではあり得る。
