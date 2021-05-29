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
Duration: 0:10:00

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
