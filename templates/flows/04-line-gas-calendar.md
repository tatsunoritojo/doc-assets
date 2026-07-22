# 04 — LINE → GAS → Google Calendar

**由来:** LINE Bot + Calendar  
**アイコン:** `brands/line.svg` `brands/googleappsscript.svg` `brands/googlecalendar.svg`

```mermaid
flowchart LR
  User[LINE User]:::actor --> LINE[LINE Platform]:::external
  LINE --> Bot[GAS Web App]:::app
  Bot --> Cal[Google Calendar]:::data
  Bot --> Reply[LINE Reply]:::external
  classDef actor fill:#EEF2FF,stroke:#6366F1,color:#111
  classDef app fill:#E8F1FF,stroke:#3B82F6,color:#111
  classDef data fill:#ECFDF5,stroke:#10B981,color:#111
  classDef external fill:#FFF7ED,stroke:#F59E0B,color:#111
```

| 段階 | 内容 |
|------|------|
| 1 | 友だち追加 / メッセージ |
| 2 | 対話で開始・終了・目標を収集 |
| 3 | Calendar にイベント作成 |
| 4 | リッチメニューで確認 |

**簡易 vs 推奨:** 簡易= GAS 直結 + ユーザー ID ホワイトリスト。推奨= 署名プロキシ（02 参照）。
