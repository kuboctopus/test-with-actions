<!--
<<< 著者注: ステップ 3 >>>
前のステップを確認した上で、このステップを開始してください。
用語を定義し、docs.github.com へのリンクを貼ってください。
-->

## ステップ 3: テストレポートのアップロード

_ワークフローの実行が完了しました! :sparkles:_

では、あるジョブの成果物を別のジョブで必要になった場合はどうすればよいでしょうか？ 組み込みの [アーティファクトストレージ](https://docs.github.com/actions/advanced-guides/storing-workflow-data-as-artifacts) を使用すると、あるジョブで作成されたアーティファクトを保存し、同じワークフロー内の別のジョブで使用できます。

アーティファクトをアーティファクトストレージにアップロードするには、GitHub によって構築されたアクション [`actions/upload-artifact`](https://github.com/actions/upload-artifact) を使用できます。

### :keyboard: アクティビティ: テストレポートのアップロード

1. ワークフローファイルを編集します。
2. `build` ジョブの `Run markdown lint` ステップを更新し、`vfile-reporter-json` を使用し、結果を `remark-lint-report.json` に出力します。
3. `build` ジョブに `upload-artifact` アクションを使用するステップを追加します。このステップでは、更新した `Run markdown lint` ステップで生成された `remark-lint-report.json` ファイルをアップロードします。
4. 新しい `build` は次のようになります。

```yml
build:
runs-on: ubuntu-latest
steps:
- uses: actions/checkout@v4

- name: Run markdown lint
run: |
npm install remark-cli remark-preset-lint-consistent vfile-reporter-json
npx remark . --use remark-preset-lint-consistent --report vfile-reporter-json 2> remark-lint-report.json

- uses: actions/upload-artifact@v4
with:
name: remark-lint-report
path: remark-lint-report.json
```

5. このブランチに変更をコミットします。
6. 約20秒待ってから、このページ（手順を実行しているページ）を更新します。[GitHub Actions](https://docs.github.com/actions) が自動的に次のステップに更新されます。

アーティファクトをストレージに送信するアップロードアクションと同様に、`build` ジョブから以前にアップロードしたアーティファクトをダウンロードするには、ダウンロードアクションを使用します。[`actions/download-artifact`](https://github.com/actions/download-artifact)。簡潔にするため、このコースではこの手順は省略します。