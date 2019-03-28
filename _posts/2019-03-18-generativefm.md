---
layout: post
title: 自動生成されたアンビエント音楽を無限に再生する『 Generative.fm 』をインストール
---

### スクリーンショット

![img](01.png)


### Generative.fm とは

-   [公式リポジトリ](https://github.com/generative-music/generative.fm)
-   [Generative.fm](https://generative.fm/) は，自動生成されたアンビエント音楽を無限に再生する Web サイトおよびソフトウェアです。インストールには Node.js と npm (もしくは yarn) が必要です。なお 2019 年 3 月現在 node-sass が ARM 系 CPU をサポートしていないため，Raspberry Pi 等では動作しません。


### 手順 (公式準拠)

1.  リポジトリを clone
    
        $ git clone https://github.com/generative-music/generative.fm
        $ git clone https://github.com/generative-music/samples.generative.fm

2.  サンプルファイルを作成する
    
    自動生成の基になるファイルを作成します。
    
        $ sudo apt install lame sox
        $ cd samples.generative.fm
        $ npm i
        $ npm run build:samples
    
    もし ``run `npm audit fix` to fix them, or `npm audit` for details`` のような警告が出たら，その指示に従って `npm audit fix` もしくは `npm audit fix --force` を実行してください。

3.  generative.fm をインストール
    
        $ cd ../generative.fm
        $ npm i


### 実行

    $ npm start

あとはブラウザで `http://localhost:9999` を開くと，公式サイトと同じように操作・再生できます。ネットの帯域を利用しないので，オフラインでも音楽を楽しむことができます。

