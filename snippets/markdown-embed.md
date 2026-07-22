# Markdown 埋め込みスニペット

## インライン

```markdown
フロー: ![user](icons/actors/user.svg) → ![sheets](icons/brands/googlesheets.svg) → ![mail](icons/ui/mail.svg)
```

GitHub README では相対パスがリポジトリルート基準。プロジェクトにコピーするなら:

```bash
cp -R ~/Github/doc-assets/icons ./docs/assets/icons
```

```markdown
![Vercel](./docs/assets/icons/brands/vercel.svg)
```

## 表

```markdown
| 層 | サービス |
|----|----------|
| ホスティング | ![Vercel](icons/brands/vercel.svg) Vercel |
| DB | ![Neon](icons/brands/neon.svg) Neon |
| 認証 | ![Google](icons/brands/google.svg) Google OAuth |
```

## HTML（幅固定・GitHub でも比較的安定）

```html
<p>
  <img src="icons/brands/vercel.svg" width="20" height="20" alt="Vercel" />
  <img src="icons/flow/arrow-right.svg" width="16" height="16" alt="→" />
  <img src="icons/brands/neon.svg" width="20" height="20" alt="Neon" />
</p>
```

## shields.io（リモート・本キット外）

```markdown
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
```

オフラインや「同じ見た目で図に並べたい」ときは本キットの SVG を優先。
