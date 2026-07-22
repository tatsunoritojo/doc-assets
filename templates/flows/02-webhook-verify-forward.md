# 02 — Webhook 検証 → 転送

**由来:** daybell（LINE → Cloud Functions → GAS）  
**アイコン:** `brands/line.svg` `brands/googlecloud.svg` `brands/googleappsscript.svg`

```mermaid
flowchart LR
  Src[External Platform]:::external --> Edge[Verify Proxy]:::app
  Edge -->|invalid| Drop[Drop / 200 empty]:::danger
  Edge -->|valid| Back[Backend / GAS]:::app
  Back --> Store[(Store / Calendar)]:::data
  classDef app fill:#E8F1FF,stroke:#3B82F6,color:#111
  classDef data fill:#ECFDF5,stroke:#10B981,color:#111
  classDef external fill:#FFF7ED,stroke:#F59E0B,color:#111
  classDef danger fill:#FEF2F2,stroke:#EF4444,color:#111
```

| 段階 | 内容 |
|------|------|
| 1 | 署名ヘッダ検証（HMAC 等） |
| 2 | 失敗は攻撃面を広げず黙殺可 |
| 3 | 成功のみ本体へ転送 + 共有 secret |
| 4 | 本体は業務処理のみ |

**注意:** GAS は HTTP ヘッダが取れない制約 → 署名は手前プロキシ必須、が定石。
