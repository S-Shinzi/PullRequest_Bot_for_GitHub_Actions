# PullRequest Bot for GitHub Actions
GitHub Actionsで動くベースブランチ以外にプッシュされたときに任意のユーザー宛にpull requestを生成するBot

## 使用方法
* `PR_bot.yml`の環境変数`BASE_BRANCH`と`REVIEWER`を設定する
* プッシュされたブランチで実行されるので、追加する際は直接master(main)に追加しないでブランチを切る
* プッシュすると自動でプルリクエストが`REVIEWER`宛に生成される。

### 使用上の注意
* ブランチを切った時点で一度リモートにプッシュすること

### 改善点
* 一度プルリクエストが生成されてから改めてプッシュするとエラーを吐き出してしまい、マージする際にエラーが出たままになってしまう(そのままマージすることは可能)

## Links
[GitHub Actionsを使って自分をReviewerにしたPRを作成する](https://www.memory-lovers.blog/entry/2022/11/18/083000#:~:text=%E8%87%AA%E5%88%86%E3%81%AEPR%E3%81%AF%E8%87%AA%E5%88%86,%E6%89%BF%E8%AA%8D%E3%81%99%E3%82%8B%E3%81%93%E3%81%A8%E3%81%AF%E3%81%A7%E3%81%8D%E3%81%BE%E3%81%9B%E3%82%93%E3%80%82)