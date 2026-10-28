---
title: "レッスン 12 - GitHub Pages でサイトをデプロイする"
description: "GitHub Copilot app を使って Pages ワークフローを構成し、その pull request をレビューして、公開された Space Quiz を確認します。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

GitHub Pages にデプロイして、Space Quiz を一般公開します。Copilot はワークフローを準備し、デプロイを案内できますが、変更をレビューし、サイトが公開されたことを確認するのはユーザーの責任です。

このレッスンでは、次の操作を行います。

- Copilot に GitHub Pages のデプロイ構成を依頼します。
- マージする前に、ワークフローと pull request をレビューします。
- デプロイの進行状況を確認し、公開されたサイトを検証します。

## シナリオ

Space Quiz はすでに GitHub リポジトリにありますが、誰もが簡単に試せる方法はまだありません。単一ファイルのサイトを GitHub Pages で公開すれば、サーバーやランタイム依存関係を追加せずに、公開 URL からアクセスできるようになります。

## Copilot にサイトのデプロイを依頼する

`space-quiz` の Copilot app セッションで、次のプロンプトを送信します。

```plaintext
このリポジトリで GitHub Pages を有効にしてください。必要であれば Web サイトをビルドし、GitHub Pages にデプロイする GitHub Actions ワークフローを作成してください。README がまだない場合は、アプリの説明とローカルでの実行方法を記載した README を追加してください。これらの変更で pull request を作成し、必須チェックに合格したらマージしてください。デプロイが成功するまで監視し、完了したら公開された Web サイトの最終 URL を報告してください。Pages を有効にしたりマージしたりする権限がない場合は、何を承認または実行する必要があるかを正確に説明してください。サイトが公開されるまで成功したと報告しないでください。
```

![3 段階の図。マージされた space-quiz の pull request、Build website・Upload artifact・Deploy to Pages の各ステップが成功した GitHub Actions の Deploy website 実行、yourname.github.io/space-quiz/ で公開された Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> このプロンプトは、エージェントに pull request の作成とマージ、およびリポジトリの Pages 設定の変更を依頼します。続行する前に、差分、デプロイ権限、GitHub の承認要求を確認してください。

## ワークフローをレビューしてデプロイを確認する

1. README は、リポジトリにまだ存在しない場合にのみ追加されていることを確認します。
2. ワークフローのビルド手順とデプロイ手順を含め、pull request の変更をレビューします。
3. 必須の pull request チェックに合格した後にのみマージします。
4. GitHub Actions のデプロイ実行が成功するまで確認します。
5. 報告された URL を開き、Space Quiz が読み込まれることを確認します。

エージェントが Pages の有効化や pull request のマージを行えない場合は、提示された具体的な手順に従います。デプロイが成功し、公開サイトが読み込まれるまで、タスクを完了したと見なさないでください。

## まとめと次のステップ

エージェントの報告だけに頼らず、Space Quiz が公開サイトとして利用できることとデプロイの成功を確認しました。[レッスン 13: レビューと次のステップ][next-lesson]に進みます。

[next-lesson]: ../13-review/
