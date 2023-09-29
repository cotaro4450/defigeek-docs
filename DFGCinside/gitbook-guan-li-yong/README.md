# Gitbook管理用

## Gitbookのドキュメント更新

GitbookのデータはGithubと同期を取っています。

* Gitbook ：主としてドキュメント更新を加えていく
* Github ：バックアップ用途であり、Github側でドキュメント更新は行わない

注意事項

* 同期でコンフリクトがあるときはGitbookが優先する

## Githubのブランチ

多言語化は、言語ごとにブランチを分けています。（Gitbook側ではそれらをコレクションとして統合しプルダウンで表示）

* master : 日本語
* english : 英語

Githubのブランチ ⇄ Gitbookのスペース　として1対1で同期します。

### 多言語の新ブランチ作成

新しくブランチを作成する際は独立ブランチとして作成します。ブランチごとにヒストリーを分けることで、コミット差分が混合しないようにします。

```git
git clone https://github.com/DeFiGeek-Community/defigeek-docs.git
cd defigeek-docs/
git checkout --orphan branch_name
git rm -rf .
git commit --allow-empty branch_name
git push origin branch_name
```

ブランチが作成できたことが確認できたら、Gitbook側で **Synchronize with Git** で作成したブランチへの連携を行います。

## 差分確認はリリース管理（予定）

多言語サイトでは、Gitbookの更新差分がどんどん分かりにくくなります。

例えば、日本語版を英語に一旦すべて翻訳完了した後、追記や修正を行っていくと、英語版への反映が漏れることが想定されます。

そのため、変更履歴をリリースとして 1.0, 1,1 のように残し、過去に翻訳完了した位置からの変更差分をコンペアで確認できるようにします。同様に、英語版は 1.0e, 1.1e のようにチェックポイントを合わせて、どこまで変更が反映できているかを明示します。



