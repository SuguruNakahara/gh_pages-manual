# GitBookの使い方

---

## デプロイ先となるリモートリポジトリの作成

まずはじめにGithubにリモートリポジトリを作成して、ローカルにクローンしておいてください。

## gitbook のインストール

次にgitbookコマンドを使用するためにgitbookをnpmを使用してインストールします。

```
npm install -g gitbook-cli
```

## mdファイルの作成

GitBookのファイル構成はとてもシンプルです。

* 「**SUMMARY.md **」：左側のタブを構成するために必要なファイル（ページとかのルール管理している？）

* 「他のmdファイル」：各ページを構成しているファイル

この２種類のファイルから成り立っていて、最後にビルドする時もこのファイルを使用します。

GitBook Editorなどを利用して必要なmdファイルを生成したら、次はビルドです。

## GitBook からドキュメントの HTML を出力

まず、上記でクローンしたところまで移動して、以下のコードを実行してください

```
cd クローン場所
gitbook init
```

こうすることでgitbookの雛形が生成されると思います。

今回は「**gitbook init**」コマンドを実行しましたが、エディターなどで自分で作成した場合は不要だと思います。

「**gitbook init**」コマンドを確認したら、生成されたmdファイルの代わりに自分で作成したmdファイルを配置して、以下のコマンドを実行してください。

```
gitbook build ./ docs/ 
```

このコマンドを実行することでdocsフォルダが生成されたと思います。

ちなみにgitbook build コマンドの第１引数はmdファイルがいる場所の指定、第２引数は書き出し場所を指定しています。

## GitHubに配置

最後にGitHubにプッシュして終わりです。
