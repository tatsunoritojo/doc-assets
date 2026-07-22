# 05 — Vercel → Neon → 外部 API

**由来:** shifree  
**アイコン:** `brands/vercel.svg` `brands/neon.svg` `brands/postgresql.svg` `brands/googlecalendar.svg`

```mermaid
flowchart LR
  Browser[Browser]:::actor --> Vercel[Flask on Vercel]:::app
  Vercel --> Neon[(Neon PostgreSQL)]:::data
  Vercel --> GCal[Google Calendar API]:::external
  Vercel --> Cron[Vercel Cron]:::muted
  Cron --> Vercel
  classDef actor fill:#EEF2FF,stroke:#6366F1,color:#111
  classDef app fill:#E8F1FF,stroke:#3B82F6,color:#111
  classDef data fill:#ECFDF5,stroke:#10B981,color:#111
  classDef external fill:#FFF7ED,stroke:#F59E0B,color:#111
  classDef muted fill:#F8FAFC,stroke:#94A3B8,color:#334155
```

| 段階 | 内容 |
|------|------|
| 1 | リクエスト → サーバレスエントリ |
| 2 | pooled / unpooled を用途で使い分け |
| 3 | 外部 API はタイムアウトと再試行を明示 |
| 4 | マイグレーションは自動追従に賭けない |

**注意:** 本番 migration は制御された単一ステップ。`/health/schema` で positive 検証。
