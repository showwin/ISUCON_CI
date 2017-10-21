# ISUCON_CI

## CI で設定する環境変数

* `IPS`: '1.1.1.1,2.2.2.2,3.3.3.3'
  * `1.1.1.1`, `2.2.2.2`, `3.3.3.3` のサーバーにデプロイする

* `SSH_KEY`: 公開鍵の中身
  * サーバーにSSHするのに使う

* `SSH_USER`: `hoge`
  * SSHするユーザ名

* `DEPLOY_DIR`: `~/`
  * `git pull origin branch_name` するディレクトリ。

* `DEPLOY_BRANCH`: `master`
  * デプロイするブランチ
