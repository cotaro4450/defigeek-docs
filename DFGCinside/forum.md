---
description: gov.defigeek.xyz で運用しているDiscourseの管理について
---

# フォーラム

## VPS

DFGCでVPSを借りて、Linux上でDiscourseアプリを動かしています。

ホスト先、リソース、権限については契約管理担当に問い合わせてください。

## Discourse

* ソースはこちらです。アップデートはGUIで可能です。\
  [https://github.com/discourse/discourse/blob/main/docs/INSTALL.md](https://github.com/discourse/discourse/blob/main/docs/INSTALL.md)
* `app.yml` ではSMTPを設定しています。
  * smtp user: team@defigeek.xyz
  * SMTP設定: [https://app.smtp2go.com/](https://app.smtp2go.com/)
* リビルド、リストアはVPSにSSHして実行してください。
  * ```
    cd /var/discourse/
    ./launcher rebuild app
    ```
* バックアップは週1で自動実行されます。
  * 引越しをするときはSSHで `app.yml`, `discourse-setup`も取得しましょう。

## Discord通知

* discourse-chat-integration プラグインを入れています。\
  [https://github.com/discourse/discourse-chat-integration](https://github.com/discourse/discourse-chat-integration)
* **設定 → プラグイン → チャットの統合** から、Discourseカテゴリごとに通知先のDiscordチャンネルを設定してください。DiscordチャンネルごとにウェブフックURLを取得します。



