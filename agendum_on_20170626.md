# 議題リスト（テーマ: エラー通知）
## サービス

### [Airbrake](https://airbrake.io)

### [Rollbar](https://rollbar.com)


#### 共有事項

- 無料枠は3000（通知するエラー件数）
- Person tracking便利そう！  
アプリソースに変更を加えることなくエラー通知内容にcurrent_userの内容を加えてくれる
- 便利: スタックとレースからgithubのソースに飛べる

#### 質問・疑問

- Uncaught exceptionsは自動的に通知されるが、caught exceptionsはどういうエラーを通知すべきか
- `#report_validation_errors_to_rollbar`ってどういうケースで使うの？
  - DDos攻撃の検知ができる？

- `Rollbar.warn`や`Rollbar.error`で任意の箇所で通知を行えるが、loggerと一緒に使うのか、片方のみ使えば済むのか。Rollbarはエラートラッキングサービスなので、loggerとは分けるべきか。`#logger_with_notification_if_log_level_is_more_critical_than_warning`のようなメソッドを作った方が良い？
```ruby
logger.error(err_msg)
Rollbar.error(err_msg)
```
みたいなのはまとめておきたい。


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

## その他

+ 狼少年のような通知を減らすために、どのような取り組みが有効か教えて欲しい
+ （Rails関係ないので時間があれば）Lambdaでのエラー通知をslackに飛ばしたりする良い方法あれば教えてください