# Radio Ghost Writer

## ゴールと数値の定義

このプロジェクトのゴール（要件定義）と数値の定義は `docs/goal/` を正本とする。

- `docs/goal/README.md` — 人が読む版（ゴール・完了条件・数値定義・開発要件）
- `docs/goal/goal.json` / `docs/goal/metrics.json` — 機械可読の現行版
- `docs/goal/CHANGELOG.md` — 版の変更履歴（過去版は `docs/goal/history/v<n>/` に保存）

ゴールや数値定義を変えるときは、このファイルではなく `docs/goal/` を
`new-project` スキル（改訂モード）で更新すること。このファイルへの直接の
手書きの進捗％・完了条件の重複記載はしない（進捗％は `docs/goal/progress.json` に置き、
`new-project` スキルの「進捗を更新して」で測る。2か所に書くと食い違う）。

<!-- git-repo
owner: levela-inc
url: https://github.com/levela-inc/Radio-Ghost-Writer
-->
