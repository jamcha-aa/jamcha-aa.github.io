---
layout: post
title: Ubuntu 18.04でqutebrowserを使う
tags: [qutebrowser, Ubuntu]
---

#### インストール

-   sudo apt install qutebrowser
    -   チートシートはこちら <https://qutebrowser.org/img/cheatsheet-big.png>

-   qutebrowserで画面内文字列をコピーするにはqutebrowser 1.3.0をインストールしましょう。必要なパッケージは18.10から拝借します (2018.05.11現在)。
    -   <https://packages.ubuntu.com/cosmic/qutebrowser>
    -   <https://packages.ubuntu.com/cosmic/qutebrowser-qtwebengine>
    -   <https://packages.ubuntu.com/cosmic/qutebrowser-qtwebkit>
    -   <https://packages.ubuntu.com/cosmic/python3-pyqt5>

#### よく使う操作

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="left" />
</colgroup>
<tbody>
<tr>
<td class="left">hjkl</td>
<td class="left">移動</td>
</tr>


<tr>
<td class="left">gg</td>
<td class="left">最上段に戻る</td>
</tr>


<tr>
<td class="left">o　</td>
<td class="left">URLを開く</td>
</tr>


<tr>
<td class="left">f</td>
<td class="left">現在のタブでリンクを開く</td>
</tr>


<tr>
<td class="left">&#xa0;</td>
<td class="left">入力フォームを選択するときにも使える</td>
</tr>


<tr>
<td class="left">F (大文字)</td>
<td class="left">新しいタブでリンクを開く</td>
</tr>


<tr>
<td class="left">d　</td>
<td class="left">タブを閉じる</td>
</tr>


<tr>
<td class="left">J (大文字)</td>
<td class="left">次のタブ</td>
</tr>


<tr>
<td class="left">H (大文字)</td>
<td class="left">戻る</td>
</tr>


<tr>
<td class="left">/</td>
<td class="left">検索</td>
</tr>


<tr>
<td class="left">&#xa0;</td>
<td class="left">ハイライトされた状態でEnterを押すと確定</td>
</tr>


<tr>
<td class="left">&#xa0;</td>
<td class="left">nで次候補へ移動</td>
</tr>


<tr>
<td class="left">v</td>
<td class="left">ビジュアルモード (キャレットモード)</td>
</tr>


<tr>
<td class="left">&#xa0;</td>
<td class="left">再度vで文字列の選択開始</td>
</tr>


<tr>
<td class="left">&#xa0;</td>
<td class="left">yでコピー</td>
</tr>


<tr>
<td class="left">&#xa0;</td>
<td class="left">コピーした文字列はppで検索</td>
</tr>


<tr>
<td class="left">:q</td>
<td class="left">終了</td>
</tr>
</tbody>
</table>

-   その他 (検索エンジンの変更など)
    -   :set で設定画面を開く

#### あとがき

exwm環境でメインブラウザとして使用しています。特別なカスタマイズをしなくても軽快な操作ができるので，「[思考のスピードでネットサーフィンが出来る](https://qiita.com/geotrader/items/47fd0a7e5783e5a0b599)」という評価は伊達じゃないと思います。
