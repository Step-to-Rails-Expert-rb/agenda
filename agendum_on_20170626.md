# 議題リスト（テーマ: エラー通知）
## サービス

### [Airbrake](https://airbrake.io)

### [Rollbar](https://rollbar.com)
* Uncaught exceptionsは自動的に通知されるが、caught exceptionsはどういうエラーを通知すべきか
+ Person tracking便利そう！  
アプリソースに変更を加えることなくエラー通知内容にcurrent_userの内容を加えてくれる

### [Raygun](https://raygun.com)

### [Sentry](https://sentry.io/welcome/)

## OSS

### [errbit](https://errbit.com)
* Airbrake APIを使ったOSSのエラー検知アプリケーション。  
OSSなのでカスタマイズして運用したい場合は有効。  
ただし運用をしなければいけないのがデメリットではある。

## その他愚痴・辛み・知見共有など
### JS のエラー検知はsource map 対応は必須。
### エラー検知を導入するメリット・デメリットは何か？
### 選定にあたっての項目候補（思いつく限り）
* 対応している言語、フレームワーク。
* エラーリミット。
* 月額料金に対しての利用プロジェクト数、ユーザ数
* 操作性（エラーを切り替えるのは容易？などなど）
* ログの保存期間
* 念の為連携できる外部サービスも確認

