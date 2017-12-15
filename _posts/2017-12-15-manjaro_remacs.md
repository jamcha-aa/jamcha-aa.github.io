---
layout: post
title: Manjaro Linuxにremacsをインストール
---

# 手順

## yaourtをインストール

    $ pacman -Syyu
    $ pacman -S yaourt

なお初期設定では，tmpディレクトリの容量制限 (1GB) のため次項のrust開発版がインストールできません。<https://gae-fan.blogspot.jp/2014/10/yaourt-tmp.html> に従ってtmpディレクトリの場所を変更しておいてください。

## Rust開発版，remacsをインストール

<div class="center">
$ yaourt remacs
</div>

yaourtはrustもまとめてインストールしてくれますが，途中で「Rustをnightlyにして」と言われます。ターミナルでtmp/makepkg/remacsに移動し，remacs公式のREADMEに書かれた次のコマンドを実行してください。

    $ cd rust_src
    $ rustup install `cat rust-toolchain`
    $ cd ../
    $ rustup override set nightly

改めてyaourtを実行します。

    $ yaourt remacs