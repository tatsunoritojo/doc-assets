# ブランド選定の考え方

`icons/brands/` に何を入れるかの目安（公開用・一般化）。

## 優先度

| 優先 | カテゴリ | 例 |
|------|----------|-----|
| S | ホスティング / ソース / 認証基盤 | Vercel, GitHub, Google, Cloudflare |
| S | データ | PostgreSQL, Neon, Sheets, SQLite |
| A | AI / エージェント | Claude, Anthropic, OpenAI, ChatGPT, Gemini |
| A | メッセージ | LINE, Slack, Discord |
| B | FW / 言語 | Next.js, React, Python, Flask, TypeScript |
| B | 周辺 SaaS | Supabase, Firebase, Netlify, Resend |
| C | エディタ / CLI 周辺 | VS Code, Playwright, Homebrew |

## 入れ方

1. [Simple Icons](https://simpleicons.org) に slug がある → 取得し brand hex でカラー化  
2. 無い → ワイヤ記号 or 図解用カスタム（公式と誤認しない）  
3. Lucide で足りる概念（user, arrow, lock）は brands に無理に入れない  

## 使わないもの

- 商標ガイドラインに反する改変ロゴ  
- 個人マシンの inventory を brands 選定の唯一の根拠にすること（参考にはしてよい）  
