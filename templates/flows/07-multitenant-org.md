# 07 — マルチテナント org 境界

**由来:** shifree / attendance-saas 方針  
**アイコン:** `actors/building.svg` `actors/users.svg` `data/database.svg`

```mermaid
flowchart TB
  Req[Request + session]:::actor --> Authz[Authorizer]:::app
  Authz -->|deny| 403[403 / empty]:::danger
  Authz -->|allow org_id| Q[Query scoped by org]:::app
  Q --> DB[(Tenant data)]:::data
  classDef actor fill:#EEF2FF,stroke:#6366F1,color:#111
  classDef app fill:#E8F1FF,stroke:#3B82F6,color:#111
  classDef data fill:#ECFDF5,stroke:#10B981,color:#111
  classDef danger fill:#FEF2F2,stroke:#EF4444,color:#111
```

| 段階 | 内容 |
|------|------|
| 1 | 認証 ≠ 認可。毎リクエストで org を解決 |
| 2 | クエリは必ず org スコープ |
| 3 | 管理 API はロール dual-check |
| 4 | 招待リンクは一回性・期限 |

**注意:** JWT に「強い認可」を焼かない（失効が難しい）。
