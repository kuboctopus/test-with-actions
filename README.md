<header>

<!--
<<< 作成者メモ: コースヘッダー >>>
1280×640 の画像、文頭大文字で書かれたコースタイトル、そして強調された簡潔な説明を含めてください。
リポジトリ設定で、テンプレートリポジトリを有効にし、1280×640 のソーシャル画像を追加し、head ブランチを自動削除してください。
オープンソースライセンスを追加してください。GitHub は MIT ライセンスを使用しています。
-->

# Actions でテストする

_プロジェクトで継続的インテグレーション (CI) を活用できるワークフローを作成します。_

</header>

<!--
<<< 作成者メモ: コース開始 >>>
開始ボタン、Actions の所要時間に関するメモ、そして受講者にこのコースを受講するべき理由を伝えてください。
-->

## ようこそ

[継続的インテグレーション](https://en.wikipedia.org/wiki/Continuous_integration) は、GitHub でテストを実行し、結果を報告することで、チームの品質基準を維持するのに役立ちます。 CI ツールはコミットをトリガーとしてビルドとテストを実行します。結果はプルリクエストで GitHub に返されます。このコースの目的は、`main` の問題を減らし、作業中のフィードバックを迅速化することです。

- **対象者**: 開発者、DevOps エンジニア、GitHub 初心者、学生、チーム。
- **学習内容**: 継続的インテグレーションとは何か、CI に GitHub Actions を使用する方法、テストを実行してテストレポートを生成するワークフローの作成方法を学びます。
- **構築するもの**: Markdown ファイルの整合性をチェックするために [remark-lint](https://github.com/remarkjs/remark-lint) を使用します。
- **前提条件**: 事前に [Hello GitHub Actions](https://github.com/skills/hello-github-actions) を修了していることを前提としています。
- **所要時間**: このコースの所要時間は 2 時間未満です。

このコースでは、以下の内容を学習します。

1. テストワークフローを追加する
2. テストを修正する
3. テストレポートをアップロードする
4. ブランチ保護を追加する
5. プルリクエストをマージする

### このコースの開始方法

[![start-course](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_owner=kuboctopus&template_name=test-with-actions&owner=%40me&name=skills-test-with-actions&description=My+clone+repository&visibility=public)

1. **「コースを開始」** を右クリックし、リンクを新しいタブで開きます。
2. 新しいタブでは、ほとんどのプロンプトが自動的に入力されます。
- オーナーとして、個人アカウントまたはリポジトリをホストする組織を選択します。
- プライベートリポジトリは [Actions の分単位での課金](https://docs.github.com/billing/managing-billing-for-github-actions/about-billing-for-github-actions) が発生するため、パブリックリポジトリを作成することをお勧めします。
- 下にスクロールし、フォームの下部にある **「リポジトリを作成」** ボタンをクリックします。
1. 新しいリポジトリが作成されたら、約 20 秒待ってからページを更新します。新しいリポジトリの README に記載されている手順に従ってください。

<footer>

<!--
<<< 著者注: フッター >>>
サポートを受けるためのリンク、GitHub ステータスページ、行動規範、ライセンスリンクを追加します。
-->

---

&copy; 2023 GitHub &bull; [行動規範](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT ライセンス](https://gh.​​io/mit)

</footer>