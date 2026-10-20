# 開発に必要な項目

`docs/goal/goal.json` の完了条件を満たすために必要な技術的な前提をまとめる。
ゴールや数値の定義そのものはここではなく `docs/goal/goal.json` / `metrics.json` に書く。

見出しの中身が決まっていない場合は、空欄のままにせず「未確定」と書き、
`docs/goal/undecided.json` に `"target": "requirements.<この見出し名>"` で対応する項目を載せる。

## 技術構成

- 言語・フレームワーク: Python / Flask
- 主要なライブラリ: anthropic, openai, supabase, google-api-python-client, PyMuPDF, youtube-transcript-api, flask-cors, gunicorn

## データ接続先

- 参照するデータ（シート・DB・API）: Supabase（articles / contexts テーブル）
- 書き込み先: Supabase、Google Drive（生成原稿のMarkdown保存）

## デプロイ先

- 環境（本番・検証）: Vercel（本番）
- デプロイ方法: GitHubリポジトリをVercelにインポートし、環境変数（ANTHROPIC_API_KEY / OPENAI_API_KEY / SUPABASE_* / SPREADSHEET_ID / GOOGLE_DRIVE_FOLDER_ID / GCP_SERVICE_ACCOUNT_JSON）を設定

## 認証・権限

- ログイン方式: 未確定
- 権限の区分: 未確定

## 非機能要件

- 想定利用者数・アクセス頻度: 未確定
- 可用性・バックアップ: 未確定
- パフォーマンス要件: 未確定

## 秘密情報の扱い

- 環境変数・鍵の保管場所: ローカルは `.env`（リポジトリ直下）、本番はVercelプロジェクトの環境変数
- リポジトリに含めないもの（`.gitignore` を参照）: `.env*`, `service_account.json`, `credentials.json`, `token.pickle`
