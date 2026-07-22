# 03 — Desktop → Sheets → GAS onChange

**由来:** Desktop + スプレッドシート運用  
**アイコン:** `brands/python.svg` `brands/googlesheets.svg` `brands/googleappsscript.svg` `ui/qr-code.svg`

```mermaid
flowchart LR
  QR[QR Scanner]:::actor --> Desk[Desktop App / Kivy]:::app
  Desk -->|gspread| Sheets[(Google Sheets)]:::data
  Sheets -->|onChange| GAS[GAS 通知・集計]:::app
  GAS --> Mail[Email / Notify]:::external
  classDef actor fill:#EEF2FF,stroke:#6366F1,color:#111
  classDef app fill:#E8F1FF,stroke:#3B82F6,color:#111
  classDef data fill:#ECFDF5,stroke:#10B981,color:#111
  classDef external fill:#FFF7ED,stroke:#F59E0B,color:#111
```

| 段階 | 内容 |
|------|------|
| 1 | QR → 学籍解決 → Sheets に append |
| 2 | 3 問回答を行更新 |
| 3 | GAS が変更検知で保護者通知 |
| 4 | ポータルは別経路で Sheets 参照 |

**注意:** Desktop は GAS HTTP を呼ばない。サービスアカウント権限が本番到達点。
