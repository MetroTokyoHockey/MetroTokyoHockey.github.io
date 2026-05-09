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
2. GitHub に push
3. GitHub Pages へ反映

## Notes

- フォーム送信の通知先メールアドレスや運用設定は `Formspree` 側で管理します
- GitHub Pages は静的ホスティングのため、サーバーサイドのメール送信処理はこのリポジトリには含まれていません
