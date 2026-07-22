# 08 — CI → Preview → Production

**由来:** PR preview → production  
**アイコン:** `brands/github.svg` `brands/vercel.svg` `status/check.svg`

```mermaid
flowchart LR
  Dev[Push / PR]:::actor --> CI[GitHub Actions]:::app
  CI -->|fail| Block[Merge block]:::danger
  CI -->|pass| Preview[Preview Deploy]:::external
  Preview --> Review[Human review]:::actor
  Review --> Prod[Production]:::app
  classDef actor fill:#EEF2FF,stroke:#6366F1,color:#111
  classDef app fill:#E8F1FF,stroke:#3B82F6,color:#111
  classDef external fill:#FFF7ED,stroke:#F59E0B,color:#111
  classDef danger fill:#FEF2F2,stroke:#EF4444,color:#111
```

| 段階 | 内容 |
|------|------|
| 1 | lint / test / build |
| 2 | PR に preview URL |
| 3 | main は protected + 必要なら reviewers |
| 4 | 業務時間帯の公開 git はガード対象 |

**注意:** production 自動デプロイを切っているリポでは workflow_dispatch を正とする。
