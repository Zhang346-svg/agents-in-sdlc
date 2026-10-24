---
title: "レッスン 12 - GitHub Pages でサイトをデプロイする"
description: "GitHub Copilot app を使って Pages ワークフローを構成し、プル リクエストをレビューして、公開された Space Quiz を確認します。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Space Quiz を GitHub Pages にデプロイして、一般に公開します。Copilot はワークフローを準備し、デプロイを案内できますが、変更をレビューしてサイトが公開されたことを確認するのはご自身の責任です。

このレッスンでは、次のことを行います。

- Copilot に GitHub Pages のデプロイ構成を依頼します。
- マージする前にワークフローとプル リクエストをレビューします。
- デプロイの進行状況を確認し、公開されたサイトを検証します。

## シナリオ

Space Quiz はすでに GitHub リポジトリにありますが、簡単に試す方法が必要です。GitHub Pages を使って単一ファイルのサイトを公開すると、サーバーやランタイム依存関係を追加せずに、公開 URL からアクセスできるようになります。

## Copilot にサイトのデプロイを依頼する

`space-quiz` の Copilot app セッションで、次のプロンプトを送信します。

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![3 段階の図: マージ済みの space-quiz プル リクエスト、Build website・Upload artifact・Deploy to Pages の各ステップが成功した GitHub Actions の Deploy website 実行、yourname.github.io/space-quiz/ で公開された Space Quiz](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> このプロンプトは、エージェントにプル リクエストの作成とマージ、およびリポジトリの Pages 設定変更を依頼します。続行する前に、diff、デプロイ権限、GitHub の承認プロンプトを確認してください。

## ワークフローをレビューしてデプロイを確認する

1. リポジトリに README がまだない場合にのみ追加されていることを確認します。
2. ワークフローのビルドおよびデプロイ手順を含め、プル リクエストの変更をレビューします。
3. 必須のプル リクエスト チェックに合格してからマージします。
4. GitHub Actions のデプロイ実行が成功するまで確認します。
5. 報告された URL を開き、Space Quiz が読み込まれることを確認します。

エージェントが Pages を有効にできない場合やプル リクエストをマージできない場合は、提示された具体的な手順に従ってください。デプロイが成功し、公開サイトが読み込まれるまで、作業を完了扱いにしないでください。

## まとめと次のステップ

Space Quiz が公開サイトとして利用できるようになり、エージェントの報告だけに頼らずデプロイを確認できました。続けて[レッスン 13: 振り返りと次のステップ][next-lesson]に進みます。

[next-lesson]: ../13-review/
