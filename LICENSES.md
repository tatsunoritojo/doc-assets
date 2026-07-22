# ライセンス

## Lucide Icons（actors / flow / status / data / infra / ui）

- 出典: https://lucide.dev
- ライセンス: ISC（上流 LICENSE を正とする）
- 単色線画のまま同梱

## Simple Icons（brands / brands-mono の大半）

- 出典: https://simpleicons.org
- ライセンス: **CC0 1.0**（SVG 形状）
- カラー版: 上流の brand hex を `fill` に焼き付けたもの
- 商標は各社に帰属。公開利用は各ガイドラインに従うこと

## 多色 Google（公式プロダクトロゴ）

Simple Icons は1形状1色しか持てず、Google プロダクトのロゴは本来の多色を再現できない。
次の6件は **Google 公式 CDN の現行デザイン**に差し替えてある（単色版は `brands-mono/` に残っている）。

| ファイル | 取得元 |
|---|---|
| `brands/googleappsscript.svg` | `https://fonts.gstatic.com/s/i/productlogos/apps_script/v1/192px.svg` |
| `brands/googlesheets.svg` | `https://fonts.gstatic.com/s/i/productlogos/sheets_2020q4/v1/192px.svg` |
| `brands/googledrive.svg` | `https://fonts.gstatic.com/s/i/productlogos/drive_2020q4/v2/192px.svg` |
| `brands/googleforms.svg` | `https://fonts.gstatic.com/s/i/productlogos/forms_2020q4/v1/192px.svg` |
| `brands/googlecalendar.svg` | `https://fonts.gstatic.com/s/i/productlogos/calendar_2020q4/v2/192px.svg` |
| `brands/gmail.svg` | `https://fonts.gstatic.com/s/i/productlogos/gmail_2020q4/v1/192px.svg` |

取得日 2026-07-23。加工は空白の畳み込みと `width`/`height` の付与のみ（形状・色は無改変）。
`brands/google.svg` は一般的な4色 G パス。いずれも Google ブランド利用規定に注意。

**未差し替え**:

- `brands/googlechrome.svg` — 公式版（`productlogos/chrome/v1/192px.svg`）は内部にラスタ画像を3枚抱えて 196KB あるため見送り。単色のまま
- `brands/python.svg` — python.org が配布するのはワードマーク入りのみで、マーク単体の公式アセットが無い。単色のまま

## 図解用カスタム

- `icons/brands/grok.svg` / `xai.svg` — Simple Icons 非掲載のため図解用に作成
- 公式ロゴ差し替えを推奨する場面では差し替えてよい

## ChatGPT / Codex

- OpenAI マーク（Simple Icons）を色分けして別名保存
- 公式が別アセットを出す場合は差し替え

## 文書

- README / catalog / snippets — 東城立憲。アイコン本体は上記が優先
