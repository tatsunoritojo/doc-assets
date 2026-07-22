# Badges スニペット

## ローカル静的（オフライン・再現性）

```markdown
![build](badges/static/build-passing.svg)
![license](badges/static/license-mit.svg)
![python](badges/static/python-311.svg)
![deploy](badges/static/deploy-vercel.svg)
```

プロジェクトにコピー:

```bash
cp -R badges/static ./docs/badges
```

### よく使う静的セット

| 用途 | ファイル |
|------|----------|
| CI OK / NG | `build-passing.svg` / `build-failing.svg` |
| テスト | `tests-passing.svg` |
| ライセンス | `license-mit.svg` / `license-private.svg` |
| 言語 | `python-311.svg` / `node-20.svg` / `typescript-5.svg` |
| デプロイ | `deploy-vercel.svg` / `deploy-netlify.svg` / `deploy-gas.svg` |
| DB | `db-neon.svg` / `db-postgresql.svg` / `db-sheets.svg` |
| 状態 | `status-production.svg` / `status-staging.svg` / `status-wip.svg` |
| AI | `ai-claude.svg` / `ai-codex.svg` / `ai-grok.svg` |
| E2E / CI | `e2e-playwright.svg` / `ci-github-actions.svg` |

---

## Shields.io 動的

変数: `{owner}` `{repo}` `{branch}`

```markdown
![CI](https://img.shields.io/github/actions/workflow/status/{owner}/{repo}/ci.yml?branch={branch}&style=flat-square)
![license](https://img.shields.io/github/license/{owner}/{repo}?style=flat-square)
![last commit](https://img.shields.io/github/last-commit/{owner}/{repo}?style=flat-square)
```

### スタック表示

```markdown
![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-deploy-000000?style=flat-square&logo=vercel&logoColor=white)
![Neon](https://img.shields.io/badge/Neon-PostgreSQL-00E599?style=flat-square&logo=neon&logoColor=black)
![Google](https://img.shields.io/badge/Google-OAuth-4285F4?style=flat-square&logo=google&logoColor=white)
![LINE](https://img.shields.io/badge/LINE-Messaging_API-00C300?style=flat-square&logo=line&logoColor=white)
```

### スタイル方針

| 用途 | style |
|------|--------|
| README 本文 | `flat-square` |
| ヒーロー | `for-the-badge`（最大 4 個） |
| オフライン | **静的 SVG** |

## プリセット例

### SaaS（Flask + Vercel + Neon）

```markdown
![deploy](https://img.shields.io/badge/deploy-Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![db](https://img.shields.io/badge/DB-Neon-00E599?style=flat-square&logo=neon&logoColor=black)
![auth](https://img.shields.io/badge/auth-Google_OAuth-4285F4?style=flat-square&logo=google&logoColor=white)
```

### GAS + Sheets

```markdown
![stack](https://img.shields.io/badge/stack-GAS_+_Sheets-34A853?style=flat-square&logo=googlesheets&logoColor=white)
![AI](https://img.shields.io/badge/AI-Claude-D97757?style=flat-square&logo=claude&logoColor=white)
```

### Next.js サイト

```markdown
![Next.js](https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
```
