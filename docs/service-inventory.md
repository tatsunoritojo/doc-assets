# Github 横断サービス観測（2026-07-23）

`doc-assets` の brands 選定根拠。書き込み前の観測のみを要約。

## 頻度 S（横断・本番に近い）

| サービス | リポ例 |
|----------|--------|
| Vercel | shifree, portfolio, hirodai-3d-site, code-concierge, tipper-*-client |
| Google Sheets / Drive / Calendar / Forms / GAS / clasp | onedrop, shifree, daybell, correspondence-school-finder |
| GitHub | ほぼ全リポ、template-gallery は Pages |

## 頻度 A

| サービス | リポ例 |
|----------|--------|
| Neon / PostgreSQL | shifree 本番, attendance-saas, kintai-system |
| Anthropic Claude | onedrop 教員レポート, sales-report-app, survey-designer, code-concierge |
| LINE | daybell_LINE_Bot, onedrop 設計, hirodai 導線 |
| Playwright | shifree, code-concierge, tipper, onedrop スライド QA |

## 頻度 B

| サービス | リポ例 |
|----------|--------|
| Netlify | correspondence-school-finder（主） |
| Firebase / Expo | habit-tracker |
| Supabase | sales-report-app, survey-designer |
| Cloudflare DNS | portfolio, correspondence-school-finder |
| Resend | correspondence-school-finder 実装 / code-concierge・tipper 想定 |
| Gemini | correspondence-school-finder / onedrop は停止寄り |
| GCP Cloud Functions | daybell 推奨構成 |
| Upstash Redis | code-concierge |
| Auth.js (next-auth) | code-concierge |
| GA4 | correspondence-school-finder, tipper 言及 |

## 既存局所キット

`onedrop/assets/diagrams/logos/` — anthropic, gmail, googleappsscript, googlecalendar, googledrive, googleforms, googlesheets, python 等。横断正本は本リポ。

## 未収録ブランド

Playwright / OpenAI / AWS — Simple Icons 取得失敗または非掲載。代替は README 参照。
