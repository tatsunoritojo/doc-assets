# Mermaid でのサービスフロー

Mermaid はローカル SVG ファイルをノード内画像として安定に埋め込めない環境が多い。  
**推奨**: ノードラベルにサービス名を書き、図の上下で本キットの SVG を並べる。

## サービスフロー雛形（テキスト）

```mermaid
flowchart LR
  Student[塾生 / QR] --> Desktop[Desktop App]
  Desktop --> Sheets[(Google Sheets)]
  Sheets --> GAS[GAS onChange]
  GAS --> Mail[保護者メール]
  Browser[Browser] --> Portal[GAS Web App]
  Portal --> Sheets
```

## SaaS（Vercel + DB + 外部 API）

```mermaid
flowchart LR
  User[User] --> Vercel[Vercel / Flask]
  Vercel --> Neon[(Neon PostgreSQL)]
  Vercel --> GCal[Google Calendar API]
  User --> OAuth[Google OAuth]
  OAuth --> Vercel
```

## LINE Bot 系

```mermaid
flowchart LR
  LINE[LINE Platform] --> CF[Cloud Functions]
  CF --> GAS[GAS Web App]
  GAS --> GCal[Google Calendar]
```

## アイコンを添える README パターン

```markdown
## 構成

| 役割 | サービス |
|------|----------|
| Edge | ![](../icons/brands/vercel.svg) Vercel |
| DB | ![](../icons/brands/neon.svg) Neon |
| 予定 | ![](../icons/brands/googlecalendar.svg) Google Calendar |

\`\`\`mermaid
flowchart LR
  A[User] --> B[Vercel]
  B --> C[Neon]
\`\`\`
```
