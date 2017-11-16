---
layout: post
title: Windows環境のEmacsでWanderlustを使ってGmailを読む
---

# 手順

## 1. [<https://jamcha-aa.github.io/2016/09/13/ntemacs.html>](https://jamcha-aa.github.io/2016/09/13/ntemacs.html)

を参考にWindows用のemacsのインストールとgnutlsの設定をしておきます。

## 2. Wanderlustのインストール

    M-x package-install wanderlust

## 3. [<http://opamp.hatenablog.jp/entry/2015/01/07/210407>](http://opamp.hatenablog.jp/entry/2015/01/07/210407)

を参考にinit.elへの記述の追加，および.wlファイルと.foldersファイルを作成しておきます。

## 4. [<http://www.otacky.jp/otaku_comm-14Q4.html>](http://www.otacky.jp/otaku_comm-14Q4.html)

を参考にhtmlメールを閲覧できるようinit.elに追加しておきます。MSYS2もしくはCygwinでw3mをインストールしておいてください。

## 動作している様子

![img](01.png)

emacs 25.1で使っています

# あとがき

Linux環境でのメールクライアントにMewを愛用しています。ただしWindowsではSSL/TLSの設定がどうしてもうまくいかなかったため，WindowsのEmacsでメールを読むのはあきらめていました。ところがWanderlustはすぐに動いてくれので，今後WindowsでのEmacs環境ではWanderlustを使おうと思います。
