# MetroTokyoHockey.github.io

GitHub Pages で公開する静的サイトです。

現在の構成:

- `index.html`: FreakTokyo アプリ向けのプライバシーポリシーページ
- お問い合わせフォーム: `Formspree` 経由で送信

## Contact Form

問い合わせフォームは GitHub Pages 単体ではメール送信できないため、`Formspree` を使っています。

送信先設定:

- Form endpoint: `https://formspree.io/f/meenrdvd`

反映箇所:

- [index.html](./index.html)
- `FORMSPREE_ENDPOINT`

## Update Flow

1. `index.html` を編集
2. `main` ブランチへ push
3. GitHub Actions の `Deploy GitHub Pages` が自動実行
4. GitHub Pages へ反映

## GitHub Pages Deploy

GitHub Pages の deploy は GitHub Actions で自動化しています。

- Workflow: `.github/workflows/deploy-pages.yml`
- Trigger: `main` への push / `workflow_dispatch`
- Deploy target: リポジトリ直下の静的ファイル一式

初回のみ、GitHub の `Settings` > `Pages` で `Source` を `GitHub Actions` に設定してください。

## Notes

- フォーム送信の通知先メールアドレスや運用設定は `Formspree` 側で管理します
- GitHub Pages は静的ホスティングのため、サーバーサイドのメール送信処理はこのリポジトリには含まれていません
