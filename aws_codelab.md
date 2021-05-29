author: taca10
summary: 【無料】AWS Cloud9でRubyの開発環境を作ろう
id: codelab-AWS-Cloud9-markdown
categories: codelab,AWSCloud9
environments: AWS
status: Published
feedback link: https://github.com/ree-rishun/codelab-zenn
analytics account:


# AWS Cloud9でRubyの開発環境を作ろう

## AWS Cloud9でRubyの開発環境を作ろう
Duration: 0:1000

### 環境構築
#### AWS Cloud9使います。

ブラウザ上で開発環境を構築することができます。<br>
クレジットカードの登録が必須となります。<br>
初めてAWSアカウントを作った人は、750時間分のAmazon EC2無料枠がついているので無料でお使いいただけます。<br>
以前にもAWSアカウントを作っていて、750時間分のAmazon EC2無料枠を超過している人は料金が発生します。<br>

[AWSのサイトはこちらです。](https://aws.amazon.com/jp/)

メールアドレスやパスワードを設定して、アカウント作成お願いします。
### AWSアカウント作成

1. AWS アカウントの作成
2. 連絡先情報を入力
3. お支払い情報を入力
4. SMS または日本語自動音声電話によるアカウント認証

[AWSアカウント作成方法](https://aws.amazon.com/jp/register-flow/)

## セキュリティ周りの設定

以下のサイトを参考にハンズオンでやっていきます。<br>
[こちら](https://qiita.com/yanyansk/items/3a989b70d2d3d49eff16)

### ルートアクセスキーの削除

ルートアカウントでログインして以下のURLにログインしてください。
https://console.aws.amazon.com/iam/home#/security_credentials

https://gyazo.com/af3ba2415d4174bc405ce9c1c85efd35


### ルートアカウントのMFA有効化

#### MFAとは

MFA（Multi-Factor Authentication、多要素認証、以下、MFA）とは、2つ以上の要素で行う認証をいいます。
メールアドレスとパスワードの認証に加えて、他の認証要素を使用することでセキュリティレベルが向上します。
https://www.cloudgate.jp/lineup/uno/multifactor-authentication.html

今回はAuthyアプリをダウンロードしてください。
[Authyアプリ](https://www.teluru.jp/posts/611)

上記の記事にも書いてある通り、認証データが引き継げるためとても便利です。

メールアドレスとパスワードが流出した際にもログインできないようにします。
[設定方法](https://console.aws.amazon.com/iam/home#/security_credentials)


### IAMグループの作成

IAMユーザーを作成する前に、IAMグループを作成します。<br>
IAMグループを作成することで、権限管理がしやすくなります。

[設定方法](https://console.aws.amazon.com/iam/home#/groups)

### IAMユーザーの作成


ルートアカウント以外にログインできるアカウント（IAMユーザー）を作成します。

[設定方法](https://console.aws.amazon.com/iam/home#/users)

ルートアカウントのMFA有効化の時と同じくIAMユーザーでもMFAを設定します。

## Cloud9環境作成

### Name environment

サービスからCloud9を検索します。<br>
「create　environment」ボタンを押します。<br>
Environment name and descriptionに名前を入力します。Nameはcloud9-rubyで、<br>
descriptionは空白で問題ありません。<br>


### Configure settings

Configure settingsは以下の画像をみながら設定をお願いします。
[設定方法](https://gyazo.com/a6abcba534ebe0df9e124bb5bf6e0334)



## Rubyの問題に挑戦しよう！

### FizzBuzz問題

「FizzBuzz問題」とは、3の倍数のときは「"fizz"」、5の倍数のときは「"buzz"」、共通の倍数のときは「"fizzbuzz"」、その他は「数値」を戻すという単純な処理です。ループ処理と分岐処理を理解していればコードを書けます。
(1から20までの数字で結構です。)

[実行結果](https://gyazo.com/fb8eaf017d93dd8234a5b7be36e795c7)
