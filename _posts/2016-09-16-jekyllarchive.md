---
layout: post
title: GitHubページにアーカイブページを作る
---

# 手続き

-   自分のgithub.ioリポジトリに書式の整ったarchive.htmlを置く
    -   私はStijn氏のHolo-alfaテーマ ([<http://steinvc.github.io/holo-alfa/>](http://steinvc.github.io/holo-alfa/)) から頂戴しました
-   GEMFILEに次の行を加える
    
        gem 'jekyll-archives'

# あとがき

org-modeにはwordpress用のorg2blogという強力なパッケージがあるのですが，gitやJekyllの学習もかねてgithubページに記事を投稿しています。今使用している[ type-theme](https://github.com/rohanchandra/type-theme/) にはアーカイブページがなかったため作成方法をまとめました。Jekyllはおろかcssの知識すらほとんどない私でも気軽におしゃれなブログを作ったり手軽に機能が追加できるのはすごい。