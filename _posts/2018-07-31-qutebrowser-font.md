---
layout: post
title: qutebrowserのWebフォントを変更する
tags: [qutebrowser]
---

### 手順


#### stylesheet.cssを作成します。今回はNoto Sansを指定します。

    /* :set content.user_stylesheets '/home/user/stylesheet.css'  */
    :not(pre):not(code) {
        font-family: Noto Sans CJK JP !important;
    }


#### qutebrowserでsetting画面を開き (`:set`)，stylesheet.cssのある場所を指定します。

![img](02.png)


#### qutebrowserを再起動します。


### 設定前

![img](01.png)


### 設定後

![img](03.png)


### あとがき

Manjaroなどでインストール後に日本語環境を導入した場合，qutebrowserを使うと，大抵のWebページでmonospaceフォントが表示されます (ManjaroだとDroid Sans ?)。見栄えが悪いので直しましょう。

**参考**

<https://www.reddit.com/r/qutebrowser/comments/8hezsb/fontswebfamily_options_dont_work_in_every_site/>

