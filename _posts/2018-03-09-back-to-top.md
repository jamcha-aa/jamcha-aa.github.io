---
layout: post
title: Gitbook.comで「一番上に戻るボタン」を表示する
tags: [GitBook]
---

# 注意

追記: Apr 17, 2018.

最新版のGitbook.comではまだ対応していないプラグインが多いようです (https://docs.gitbook.com/what-is-new/important-differences#plugins)。

# 手順

ボタンを追加したいリポジトリにbook.jsonというファイルを作成し，以下の内容で保存します。あとはGitbookが自動でプラグインをインストールして設定してくれます。

    {
        "plugins" : [ "back-to-top-button" ]
    }

作者のリポジトリ: <https://github.com/stuebersystems/gitbook-plugin-back-to-top-button>

# あとがき

Gitbook.comで公開するページには「一番上に戻るボタン」が標準でついていません。そこで調べたところ，柔軟な仕組みのおかげで簡単に設置することができました。stuebersystems氏に感謝。

なお，目次をフロート型にするなど，より多機能なプラグインも公開されています (<https://plugins.gitbook.com/plugin/anchor-navigation-ex-eus>)。

参考: <http://www.travelbanana.net/entry/backtotop>