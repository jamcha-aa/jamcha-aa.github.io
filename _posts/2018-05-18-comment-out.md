---
layout: post
title: 小説などの文章からコメントを削除して出力する
---

# 例

今回はこのファイル (sample.txt) からコメント行を消します。

**sample.txt**

> 事件の流れ〜
> 
> */ 犯人
> /* トリック
> 
> 取り調べ〜
> 
> // 推理のパターンB
> 
> 解決に至るまで〜
> 
> // 犯人の扱い
> 
> おわり

# ファイルのある場所でターミナルを起動

ターミナルの開き方がわからない場合は[こちら](https://book.mynavi.jp/macfan/detail_summary/id%3D41833)を参照。

**入力するコマンド**

    $ sed -e "/\/\//d" sample.txt > sample-r.txt

# 結果

**sample-r.txtの中身**

> 事件の流れ〜
> 
> 取り調べ〜
> 
> 解決に至るまで〜
> 
> おわり

# あとがき

sedはMacでも使えます。WindowsはWindows Subsystem for Linuxを入れてください。
