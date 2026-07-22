# 10 — AI レポート生成（スロット接地）

**由来:** 接地付き AI レポート  
**アイコン:** `brands/claude.svg` `brands/anthropic.svg` `brands/googlesheets.svg`

```mermaid
flowchart LR
  Facts[Facts / metrics from Sheets]:::data --> Slot[Slot builder]:::app
  Slot --> LLM[Claude API]:::external
  LLM --> Validate[Validate / no invent]:::app
  Validate -->|fail| Retry[Repair or reject]:::danger
  Validate -->|ok| UI[Report UI]:::app
  classDef app fill:#E8F1FF,stroke:#3B82F6,color:#111
  classDef data fill:#ECFDF5,stroke:#10B981,color:#111
  classDef external fill:#FFF7ED,stroke:#F59E0B,color:#111
  classDef danger fill:#FEF2F2,stroke:#EF4444,color:#111
```

| 段階 | 内容 |
|------|------|
| 1 | 数値はスロット。モデルに生データ丸投げしない |
| 2 | system で創作禁止・根拠必須 |
| 3 | 出力検証（句点・禁止語・探索モード制約） |
| 4 | 最終判断は教員。UI にその旨 |

**注意:** 学習利用ポリシーで Gemini 無料枠に実データを流さない判断あり。Claude と Anthropic ロゴは別ファイル。
