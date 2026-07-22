# 09 — 障害時 Plan B（読み取り / 切り戻し）

**由来:** 障害対応テンプレ + shifree 復旧経験  
**アイコン:** `status/error.svg` `status/warn.svg` `infra/shield.svg`

```mermaid
flowchart TB
  Alert[症状観測]:::danger --> Impact[業務影響 1 行]:::danger
  Impact --> B[Plan B 復旧]:::app
  Impact --> A[Plan A 原因]:::muted
  B --> RO[Read-only / 旧版 / 手動 SQL]:::data
  A --> Fix[修正 + 検証]:::app
  Fix --> Verify[Positive 検証]:::app
  RO --> Verify
  classDef app fill:#E8F1FF,stroke:#3B82F6,color:#111
  classDef data fill:#ECFDF5,stroke:#10B981,color:#111
  classDef danger fill:#FEF2F2,stroke:#EF4444,color:#111
  classDef muted fill:#F8FAFC,stroke:#94A3B8,color:#334155
```

| 段階 | 内容 |
|------|------|
| 1 | 誰が何にアクセスできないか（業務語彙） |
| 2 | Plan B を先に（読み取り専用 DB・旧デプロイ） |
| 3 | Plan A は並行（ログ・スキーマ） |
| 4 | 復旧定義を先に書いてから「完了」 |

**注意:** コールドスタート自動 migrate 再有効化で再発させない。
