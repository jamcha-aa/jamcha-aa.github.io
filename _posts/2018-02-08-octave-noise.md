---
layout: post
title: GNU Octaveでホワイトノイズを作成して聴く
---

# はじめに

-   個人利用の範囲であれば <http://mc2method.org/white-noise/> に作成済みのファイルがあります。youtubeにもたくさんあります。
-   marpacなどホワイトノイズを発生させる機器が市販されているほか，[自作した方もいます](http://nomolk.hatenablog.com/entry/2018/02/02/223000)。

# 手順

## ホワイトノイズ音声の作成

octaveをインストールしておいてください。debian系のlinuxならsudo apt install octaveでインストールできます。

octaveを起動したら，コマンドウインドウで次のように入力します。

    white=rand(48000*100,2)-1;
    audiowrite('WhiteNoise.wav',white,48000);

1行目の100が配列の大きさ，2行目の48000が周波数です ([参考](https://bagustris.wordpress.com/2011/10/18/generating-white-noise-sound-on-octave-matlab-2/))。octaveを起動した場所にWhiteNoise.wavというファイルが出力されるので好きなソフトでエンコードするなり聴くなりしてください。なお1行目の2を1にするとモノラル音声になります。

私は低い音を聴きたかったため次のような音声を作成しました。

    w1=rand(11050*100,2)*.5-1;
    w2=rand(11050*100,2)*.5-1;
    w3=(w1+w2)/2;
    audiowrite('WhiteNoise.wav',white,2205);

## mpvでループ再生する場合

    mpv --loop=inf WhiteNoise.wav

ピッチを変えたい場合は次のとおり。

    mpv --loop=inf --audio-pitch-correction=no --speed=0.5 WhiteNoise.wav

speedの値でピッチを変更できます。

## あとがき

スピーカーから流せば，ヘッドホンを使用しなくても周囲の雑音を相殺できるのでおすすめです。またoctaveからportaudioで直接再生することもできますが，手間がかかるので今回は見送りました。