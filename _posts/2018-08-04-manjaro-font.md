---
layout: post
title: Manjaroのデフォルトフォントを変更する
tags: [Manjaro]
---

### 手順

※ `noto-fonts-cjk` をインストールしていない場合は先にインストールしておいてください。

    $ mkdir ~/.config/fontconfig
    $ nano ~/.config/fontconfig/fonts.conf

fonts.confの中身は [ArchWikiの「フォント設定/サンプル#日本語フォント」](https://wiki.archlinux.jp/index.php/%E3%83%95%E3%82%A9%E3%83%B3%E3%83%88%E8%A8%AD%E5%AE%9A/%E3%82%B5%E3%83%B3%E3%83%97%E3%83%AB#.E6.97.A5.E6.9C.AC.E8.AA.9E.E3.83.95.E3.82.A9.E3.83.B3.E3.83.88) をそのままコピペします。

なお以下のソースの著作権はArch Linux JP Projectにあります。

    <?xml version='1.0'?>
    <!DOCTYPE fontconfig SYSTEM 'fonts.dtd'>
    <fontconfig>
    
    <!-- Default font (no fc-match pattern) -->
     <match>
      <edit mode="prepend" name="family">
       <string>Noto Sans</string>
      </edit>
     </match>
    
    <!-- Default font for the ja_JP locale (no fc-match pattern) -->
     <match>
      <test compare="contains" name="lang">
       <string>ja</string>
      </test>
      <edit mode="prepend" name="family">
       <string>Noto Sans CJK JP</string>
      </edit>
     </match>
    
    <!-- Default sans-serif font -->
     <match target="pattern">
       <test qual="any" name="family"><string>sans-serif</string></test>
       <!--<test qual="any" name="lang"><string>ja</string></test>-->
       <edit name="family" mode="prepend" binding="same"><string>Noto Sans</string>  </edit>
     </match>
    
    <!-- Default serif fonts -->
     <match target="pattern">
       <test qual="any" name="family"><string>serif</string></test>
       <edit name="family" mode="prepend" binding="same"><string>Noto Serif</string>  </edit>
       <edit name="family" mode="append" binding="same"><string>IPAPMincho</string>  </edit>
       <edit name="family" mode="append" binding="same"><string>HanaMinA</string>  </edit>
     </match>
    
    <!-- Default monospace fonts -->
     <match target="pattern">
       <test qual="any" name="family"><string>monospace</string></test>
       <edit name="family" mode="prepend" binding="same"><string>Inconsolatazi4</string></edit>
       <edit name="family" mode="append" binding="same"><string>IPAGothic</string></edit>
     </match>
    
    <!-- Fallback fonts preference order -->
     <alias>
      <family>sans-serif</family>
      <prefer>
       <family>Noto Sans</family>
       <family>Open Sans</family>
       <family>Droid Sans</family>
       <family>Ubuntu</family>
       <family>Roboto</family>
       <family>NotoSansCJK</family>
       <family>Source Han Sans JP</family>
       <family>IPAPGothic</family>
       <family>VL PGothic</family>
       <family>Koruri</family>
      </prefer>
     </alias>
     <alias>
      <family>serif</family>
      <prefer>
       <family>Noto Serif</family>
       <family>Droid Serif</family>
       <family>Roboto Slab</family>
       <family>IPAPMincho</family>
      </prefer>
     </alias>
     <alias>
      <family>monospace</family>
      <prefer>
       <family>Inconsolatazi4</family>
       <family>Ubuntu Mono</family>
       <family>Droid Sans Mono</family>
       <family>Roboto Mono</family>
       <family>IPAGothic</family>
      </prefer>
     </alias>
    
     <dir>~/.fonts</dir>
    </fontconfig>

