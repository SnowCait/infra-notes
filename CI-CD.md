# CI/CD

## なぜ CI/CD をするのか
### Unit Test, Feature Test
- コードにバグがないか常に監視できる
- テストをするタイミング
  - PR が送られたとき
    - PR のブランチでのテスト
    - マージ先のブランチを PR のブランチへ逆マージしてテスト
  - PR がマージされたとき
    - PR が送られたときのテストからマージまで間が開くので再度テストする

### CD
- 手動でやるとヒューマンエラーが発生する
- コスト削減
  - 手動でやるとコストが高い

### 全般
- コードとして表せる
  - バージョン管理できる
- ログが残る
  - 後で調査ができる

## Services
- [GitHub Actions](https://github.com/SnowCait/git-notes/blob/master/GitHubActions.md)
- https://circleci.com/
- https://coveralls.io/
- https://app.wercker.com/
- https://www.cloudbees.com/ (Jenkins)
- https://fastlane.tools/
- [Argo CD - Declarative GitOps CD for Kubernetes](https://argoproj.github.io/argo-cd/)
- [Bitrise - Mobile Continuous Integration and Delivery](https://www.bitrise.io/)
- [Drone CI – Automate Software Testing and Delivery](https://www.drone.io/)

## 注意点
- サーバー負荷の観点から CD サーバーと CI サーバーは物理的に分ける
  - CI による負荷上昇で CD ができなくなることを防ぐ

## CI
- unit test
- resource usage (cpu, memory)

## CD
- deployment
