# 01 — Google OAuth ログイン

**由来:** SaaS Web アプリの典型  
**アイコン:** `brands/google.svg` `brands/vercel.svg`

```mermaid
flowchart LR
  U[User / Browser]:::actor --> App[App on Vercel]:::app
  App --> OAuth[Google OAuth]:::external
  OAuth --> App
  App --> Sess[Session / Cookie]:::data
  classDef actor fill:#EEF2FF,stroke:#6366F1,color:#111
  classDef app fill:#E8F1FF,stroke:#3B82F6,color:#111
  classDef data fill:#ECFDF5,stroke:#10B981,color:#111
  classDef external fill:#FFF7ED,stroke:#F59E0B,color:#111
```

| 段階 | 内容 |
|------|------|
| 1 | アプリが認可 URL へリダイレクト |
| 2 | Google 同意（スコープは最小） |
| 3 | callback で code → token |
| 4 | セッション確立（JWT に認可を焼きすぎない） |

**注意:** redirect_uri は本番と完全一致。Vercel env は `printf` で投入（末尾改行注意）。
