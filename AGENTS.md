# AGENTS.md — AI エージェント向け編集ガイド

このリポジトリは満足亮 / Ryo Manzoku の正準個人サイト（https://rmanzoku.net/ 、GitHub Pages 配信）です。

## まず読む

- 編集の詳細手順・事実ルール・同期チェックリストの正本は、workspace リポジトリ（github.com/rmanzoku/workspace）の Skill `rmanzoku-net`
- answer space の観測・測定は workspace の Skill `geo-update`（このリポジトリでは行わない）

## 絶対ルール

- **main へ直 push しない**。常にブランチ + PR（merge = 公開承認）
- **新しい事実主張（経歴・役職・実績・日付・読み）を推測で書かない**。出典は、公開済みのサイト内容、本人の明示、一次ソース URL のいずれかに限る
- このリポジトリには**静的公開ファイルのみ**を置く。スクリプト・skill・作業メモは workspace 側。直下のファイルはすべて https://rmanzoku.net/ で公開される
- PR 本文も公開される。内部パス・非公開情報を書かない

## 編集時の同期チェックリスト

- JSON-LD（Person）は `index.html` と `about/index.html` の 2 箇所。**常に両方を更新**する
- ページの追加・削除・改名: ナビとフッター（全ページ共通）、`sitemap.xml`（`<loc>`/`<lastmod>`）、`llms.txt`、旧 URL への転送スタブ（meta refresh + canonical + noindex）
- 内容変更したページの `Last updated` と sitemap `<lastmod>` を更新する
- 命名規約: title 接尾辞 `<Label> - Ryo Manzoku / 満足亮`、eyebrow はナビラベルと一致

## 検証（PR 前に必須）

workspace チェックアウトがある環境:

```bash
python3 /Users/rmanzoku/ghq/github.com/rmanzoku/workspace/scripts/validate_rmanzoku_net.py .
```

無い環境では同等の検証（全ページ HTML parse、JSON-LD の json.loads、内部リンク解決、sitemap XML parse と loc↔ファイル整合）を行うこと。
