---
layout: post
title: Gitbook.comで「一番上に戻るボタン」を表示する
---

# 手順

-   ボタンを追加したいリポジトリにbook.jsonというファイルを作成し，以下の内容で保存します。
    
        {
            "plugins" : [ "back-to-top-button" ]
        }

-   あとはGitbookが自動でプラグインをインストールしてくれます。


# あとがき

Gitbook.comで公開するページには「一番上に戻るボタン」が標準でついていません (cf. [「一番上に戻るボタン」付けてないブログ、やり方教えてやるから今すぐ付けろ。読みにくいんだよ](http://www.travelbanana.net/entry/backtotop))。そこで調べたところ，ファイルを一つ作るだけで済んだので紹介してみました。

