---
layout: post
title: magitで過去のコミットからブランチを作ってマージする
tags: [Emacs, Magit]
---

# はじめに

[Remacs](https://github.com/Wilfred/remacs)を32bit CPUの古いノートPCに入れて動かしています。スペックが低いせいか，[私が使っている環境](https://github.com/jamcha-aa/init)ではpowerlineが重かったので，導入以前に使っていたシンプルなモードラインをgitの履歴から復活させることにしました。


# 手順


## 過去のコミットからブランチを作成

M-x magit-statusでmagitを呼び出し，l, bを押して履歴を表示します。

![img](02.png)

<br>
履歴画面では逐次検索ができるので「powerline」で検索すると，該当するコミットが見つかりました。

![img](03.png)

<br>
powerline以前に使用していたものは，その1つ前のコミットまで残っているはずです (色が違う部分)。

![img](04.png)

<br>
b, 次いでcを押し，ブランチを作成します。対象は普段使っているmasterなどでなく，コミット番号の上7桁になります。

![img](05.png)

<br>
ブランチ名はGPModelineにしました。

![img](06.png)

<br>
ブランチを作成すると自動的にチェックアウトされます。画面上半分を更新すると，当時残っていたファイルも復活しているのがわかります。

![img](07.png)


## 内容を更新し，masterブランチにマージする

最新のコミットに残したい部分のみ修正します。ここではpowerline以前に使っていたmode-line-linux.elを残したいので，gp-mode-line-linux.elという名前に変更しました。

![img](08.png)

<br>
magit-statusを再び開くと，変更点が表示されるので，ふだんと同じ手続きでコミットしましょう。

![img](09.png)

<br>
Untracked filesの上でsを押し，

![img](10.png)

<br>
cを2回押してコミットメッセージを書き，

![img](11.png)

<br>
"Ctrl+c"を2回押してコミット完了です。

![img](12.png)

<br>
ここからmasterブランチにうつって，先のコミットを取り込むことにします。bを2回押してmasterにチェックアウトしましょう。

![img](13.png)

<br>
masterにチェックアウトしました。

![img](14.png)

<br>
コミットのマージにうつります。mを2回押し，取り込みたいブランチを選んでからEnterを押しましょう (ここではGPModeline)。

![img](15.png)

<br>
masterブランチにマージされました。

![img](16.png)

<br>
すぐ使えるように，init.elにモードライン用の設定を追加し，コミットしました。なおローカルのGitリポジトリであればこれで終了です。

![img](17.png)

<br>
準備ができたら，Shift-P，続いてuを押してリモートにプッシュします。

![img](18.png)

<br>
プッシュ完了後にl，bを押してgitの履歴を見ると，無事に取り込まれていることがわかります。

![img](19.png)

