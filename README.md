# 水曜のDX道場 — GitHub MCP ハンズオン用リポジトリ

**テーマ**：GitHub MCP を使って、ブランチ → Pull Request → マージ → 自動デプロイ を体験する

このリポジトリは 1 ページの静的サイトです。`main` ブランチに push されると
GitHub Actions が起動し、GitHub Pages に自動で公開されます。

## 構成

```
.
├── index.html                  # 公開されるページ（ハンズオンで編集する）
├── style.css
├── .github/workflows/deploy.yml  # 自動デプロイのワークフロー（コメント付き）
└── README.md
```

## 事前準備（各自 5 分）

1. GitHub アカウントを作成しログインしておく
2. このリポジトリを **Fork**（右上の Fork ボタン → 自分のアカウントへ）
3. Fork したリポジトリで **Settings → Pages → Source を「GitHub Actions」** に変更
4. Fork したリポジトリで **Actions タブ → 「I understand my workflows, go ahead and enable them」** をクリック
5. Claude（Desktop または claude.ai）で GitHub コネクタを接続し、自分のアカウントを認可

## ハンズオンの流れ

詳細は当日配布の `02_handson_guide.md` を参照。

| # | やること | 体験する概念 |
|---|---|---|
| 1 | Claude に「自分のリポジトリ一覧を見せて」 | MCP でツール呼び出し |
| 2 | `staging` ブランチを作る | Branch |
| 3 | `staging` 上で `index.html` のメッセージを書き換える | Commit / Push |
| 4 | `staging` → `main` の Pull Request を作る | PR |
| 5 | PR をマージする | Merge |
| 6 | Actions タブでワークフローの実行を見る | トリガー（push で発火）/ Linux ランナー |
| 7 | 公開 URL でページを確認 | 自動デプロイ |

## 公開 URL

`https://<あなたのユーザー名>.github.io/<リポジトリ名>/`
