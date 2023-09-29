---
description: xxx@defigeek.xyz のメアドを作る方法
---

# メールアドレス作成

## Email Forwarding

⚠️これはDNS管理者の設定手順です。

DNS（njal.la）で、DNS Settingsの中からEmail Forwardingを選んで作成する。&#x20;

付与する相手から事前に以下の情報をもらっておく。&#x20;

* アカウント名　※ xxxx@defigeek.xyz の xxxx の部分
* 転送先メールアドレス　※Gmailを想定

## SMTPアカウント作成

⚠️これはSMTPリレーサーバ管理者の設定手順です。

SMTP2GOに行く [https://app.smtp2go.com/](https://app.smtp2go.com/)

ダッシュボードで **Settings** → **SMTP Users** → **Add SMTP User** に進む。

{% embed url="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FYer9wYeWiRzWHX4llDJO%2Fuploads%2FimHvcNGE3WpAUGDBFXui%2Fsmtp2go-1.png?alt=media&token=f5e0a753-711e-4b05-b478-5fcfc00fff62" %}

**Username** にアカウント名を入力し、**Password**（自動生成される）を一緒にメモしておく。**Add SMTP User** で完了。

{% embed url="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FYer9wYeWiRzWHX4llDJO%2Fuploads%2FsEI9WR0n9WUa8DYyI4M6%2Fsmtp2go-2.png?alt=media&token=d5589fb7-e37a-4822-9a70-4e2fac638afb" %}

**Username**、**Password**と、**下記の設定方法**をメール利用者に渡す。

## メールクライアント設定（Gmail）

ℹ️これは利用者側の設定手順です。

Email Forwardingで設定した「転送先メールアドレス」の管理画面で行います。Gmailでは次の通りです。

1. Gmailを開く
2. 右上の歯車マークで「設定」を開く
3. すべての設定を表示
4. 「アカウントとインポート」タブを開く
5. 「名前: (Gmail を使用して他のメール アドレスからメールを送信します)」の欄で、「他のメール アドレスを追加」をクリック
6. １画面目
   1. 名前: （表示したい名前）
   2. メール アドレス: **xxxx@defigeek.xyz**
   3. 「エイリアスとして扱います。」のチェックは外す
7. ２画面目
   1. SMTP サーバー: **mail.smtp2go.com**　　ポート: **587**
   2. ユーザー名: **xxxx@defigeek.xyz**
   3. パスワード: **\<SMTP2GO作成時に渡されたパスワード>**
   4. TLS を選択
8. ３画面目
   1. 確認コードが xxxx@defigeek.xyz に送られる
   2. その数字9桁を入力

以上で設定完了です。xxxx@defigeek.xyz にテストメールを送信し、自分のGmailアカウントに受信するかテストしましょう。
