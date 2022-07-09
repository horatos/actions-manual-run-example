# GitHub Actionsのワークフローを手動実行する例

GitHub Actionsのワークフローは`workflow_dispatch`イベントを受け取るように設定することで手動で実行できる。

下記URLのGitHubのドキュメントに記載された例をそのままワークフローとして設定する。

https://docs.github.com/ja/actions/using-workflows/events-that-trigger-workflows#workflow_dispatch

このワークフローでは`workflow_dispatch`が`environment`を要求するので、リポジトリの"Settings"から"Environment"を作成する必要がある。一部のプランを除いてパブリックリポジトリでなければ作成できない。

GitHub CLIで実行する場合は以下のようなコマンドによって実行できる。

```
gh workflow run manual.yml -f environment=development -f tags=false
```
