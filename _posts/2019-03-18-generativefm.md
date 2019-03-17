---
layout: post
title: 自動生成されたアンビエント音楽を無限に再生する『 Generative.fm 』をインストール
---

### スクリーンショット

![img](01.png)


### Generative.fm とは

-   [公式リポジトリ](https://github.com/generative-music/generative.fm)
-   [Generative.fm](https://generative.fm/) は，自動生成されたアンビエント音楽を無限に再生する Web サイトおよびソフトウェアです。インストールには Node.js と yarn (もしくは npm) が必要です。


### 手順 (公式準拠)

    $ git clone https://github.com/generative-music/generative.fm
    $ cd generative.fm
    $ yarn install


### 実行

    $ yarn start

あとはブラウザで `http://localhost:9999` を開くと，公式サイトと同じように操作・再生できます。ネットの帯域を利用しないので，オフラインでも音楽を楽しむことができます。

