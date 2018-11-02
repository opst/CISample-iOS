# 証明書とプロビジョニングプロファイル
Fastlane matchを用いて管理と運用を行なっている。各自の環境にFastlaneをインストールすること。
以下のコマンドでFastlaneをインストールできる。
> gem install fastlane

## Fastlane matchの実行に必要なアカウント
ios-developers-admin@opst.co.jp

## Fastlane利用における資料
- 手順書
https://docs.google.com/document/d/1QOq6cf6uOg7rnbhx2a21WVInHv0ByVxnFzCMxlcJYV4/edit
- アカウント情報
https://docs.google.com/document/d/1hscHZmdjh4voU_U6RssVngnVLm6SMoTXrdndt1CeTbE/edit
- SSH
https://drive.google.com/drive/folders/1FYDsSPIcfmqkEczPkKrZ9CM8BRfmPYXe

## 開発用
> fastlane match development \
> --git_url git@github-opst-ios-developers:opst/ioscertificates.git \
> --git_user_email ios-developers@opst.co.jp \
> --team_id T7BG65JB87 \
> --app_identifier jp.co.opst.CISample \
> --readonly true

## 配布用
> fastlane match enterprise \
> --git_url git@github-opst-ios-developers:opst/ioscertificates.git \
> --git_user_email ios-developers@opst.co.jp \
> --team_id T7BG65JB87 \
> --app_identifier jp.co.opst.CISample \
> --readonly true

# Bitrise
## プロジェクトの作成
- BacklogのGitレポジトリはSSHを指定する。
- opst@opst.git.backlog.jp:/STD_LAB/CISample-iOS.git
- 公開鍵を設定する。

## 証明書とプロビジョニングプロファイルのアップロード
- Workflow→Code Signing

## Access Tokenの生成
- https://app.bitrise.io/me/profile#/security
