# Badges スニペット

## ローカル静的（オフライン・再現性）

パス基準: `~/Github/doc-assets/badges/static/`

```markdown
![build](/Users/tatsu/Github/doc-assets/badges/static/build-passing.svg)
![license](/Users/tatsu/Github/doc-assets/badges/static/license-mit.svg)
![python](/Users/tatsu/Github/doc-assets/badges/static/python-311.svg)
![deploy](/Users/tatsu/Github/doc-assets/badges/static/deploy-vercel.svg)
```

プロジェクトにコピーする場合:

```bash
cp -R ~/Github/doc-assets/badges/static ./docs/badges
```

```markdown
![build](./docs/badges/build-passing.svg)
```

### よく使う静的セット

| 用途 | ファイル |
|------|----------|
| CI OK / NG | `build-passing.svg` / `build-failing.svg` |
| テスト | `tests-passing.svg` |
| カバレッジ | `coverage-90.svg` / `coverage-unknown.svg` |
| ライセンス | `license-mit.svg` / `license-private.svg` |
| 言語 | `python-311.svg` / `node-20.svg` / `typescript-5.svg` |
| FW | `nextjs-16.svg` / `flask-3.svg` / `django-5.svg` |
| デプロイ | `deploy-vercel.svg` / `deploy-netlify.svg` / `deploy-gas.svg` |
| DB | `db-neon.svg` / `db-postgresql.svg` / `db-sheets.svg` |
| 状態 | `status-production.svg` / `status-staging.svg` / `status-wip.svg` |
| AI | `ai-claude.svg` / `ai-codex.svg` / `ai-grok.svg` |
| E2E / CI | `e2e-playwright.svg` / `ci-github-actions.svg` |

---

## Shields.io 動的（オンライン）

変数: `{owner}` `{repo}` `{branch}`

### 定番

```markdown
![CI](https://img.shields.io/github/actions/workflow/status/{owner}/{repo}/ci.yml?branch={branch}&style=flat-square)
![license](https://img.shields.io/github/license/{owner}/{repo}?style=flat-square)
![last commit](https://img.shields.io/github/last-commit/{owner}/{repo}?style=flat-square)
![release](https://img.shields.io/github/v/release/{owner}/{repo}?style=flat-square)
![stars](https://img.shields.io/github/stars/{owner}/{repo}?style=flat-square)
```

### スタック表示（logo 付き）

```markdown
![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-deploy-000000?style=flat-square&logo=vercel&logoColor=white)
![Neon](https://img.shields.io/badge/Neon-PostgreSQL-00E599?style=flat-square&logo=neon&logoColor=black)
![Google](https://img.shields.io/badge/Google-OAuth-4285F4?style=flat-square&logo=google&logoColor=white)
![LINE](https://img.shields.io/badge/LINE-Messaging_API-00C300?style=flat-square&logo=line&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-DD2C00?style=flat-square&logo=firebase&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=claude&logoColor=white)
```

### for-the-badge 風（ヒーロー向け・多めにしない）

```markdown
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
```

### スタイル方針（キット既定）

| 用途 | style |
|------|--------|
| README 本文・状態 | `flat-square` |
| ヒーロー 1 行だけ | `for-the-badge`（最大 4 個） |
| オフライン / 提案書 PDF | **静的 SVG** |

---

## 東城リポ向けプリセット

### shifree

```markdown
![deploy](https://img.shields.io/badge/deploy-Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![db](https://img.shields.io/badge/DB-Neon-00E599?style=flat-square&logo=neon&logoColor=black)
![auth](https://img.shields.io/badge/auth-Google_OAuth-4285F4?style=flat-square&logo=google&logoColor=white)
![python](https://img.shields.io/badge/Python-Flask-3776AB?style=flat-square&logo=python&logoColor=white)
```

### onedrop

```markdown
![stack](https://img.shields.io/badge/stack-GAS_+_Kivy_+_Sheets-34A853?style=flat-square&logo=googlesheets&logoColor=white)
![AI](https://img.shields.io/badge/AI-Claude-D97757?style=flat-square&logo=claude&logoColor=white)
![license](/Users/tatsu/Github/doc-assets/badges/static/license-private.svg)
```

### portfolio / hirodai-3d-site

```markdown
![Next.js](https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
```
