# 06 — 保護者通知メール

**由来:** onedrop 出席 GAS  
**アイコン:** `brands/gmail.svg` `brands/googleappsscript.svg` `brands/googlesheets.svg`

```mermaid
flowchart LR
  Event[入退室イベント]:::data --> GAS[GAS Trigger]:::app
  GAS --> Gate{送信条件}:::muted
  Gate -->|OK| Mail[MailApp / 通知]:::external
  Gate -->|skip| Log[ログのみ]:::muted
  Mail --> Parent[保護者]:::actor
  classDef actor fill:#EEF2FF,stroke:#6366F1,color:#111
  classDef app fill:#E8F1FF,stroke:#3B82F6,color:#111
  classDef data fill:#ECFDF5,stroke:#10B981,color:#111
  classDef external fill:#FFF7ED,stroke:#F59E0B,color:#111
  classDef muted fill:#F8FAFC,stroke:#94A3B8,color:#334155
```

| 段階 | 内容 |
|------|------|
| 1 | Sheets 変更 or 明示トリガ |
| 2 | 重複送信・テスト ID 除外 |
| 3 | 文言は運用マニュアルと一致 |
| 4 | 失敗は握り潰さずログ |

**注意:** 個人情報。ログに本文フルを残さない。
