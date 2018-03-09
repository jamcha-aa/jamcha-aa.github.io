---
layout: post
title: Gitbook.comで「一番上に戻るボタン」を表示する
---

# 手順

ボタンを追加したいリポジトリにbook.jsonというファイルを作成し，以下の内容で保存します。あとはGitbookが自動でプラグインをインストールして設定してくれます。

    {
        "plugins" : [ "back-to-top-button" ]
    }

# あとがき

Gitbook.comで公開するページには「一番上に戻るボタン」が標準でついていません。そこで調べたところ，ファイルを一つ作るだけで済みました。なお，目次をフロート型にするなど，より高機能なプラグインも公開されています (<https://plugins.gitbook.com/plugin/anchor-navigation-ex-eus>)。

参考: <http://www.travelbanana.net/entry/backtotop>