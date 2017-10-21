# ISUCON_CI

## 事前準備
* デプロイ先のインスタンスの中で `git pull origin branch` ができること
* デプロイ時に実行するコマンドを `$DEPLOY_DIR/deploy.sh` に定義しておくこと
* CIで設定する `SSH_KEY` で `SSH_USER` としてSSHログインできること

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

# 注意事項
* `DEPLOY_BRANCH` とCIで実行しているブランチ名が同じ時のみデプロイされる。つまり`DEPLOY_BRANCH=master`のときには master ブランチにpushされたときのみデプロイ処理が走る
