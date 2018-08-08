---
layout: post
title: EXWMでマルチディスプレイ
---

今回は解像度1366x768のノートPCと液晶モニタを接続してみます。[exwm Wiki](https://github.com/ch11ng/exwm/wiki#randr-multi-screen) に書かれている方法で済んだ場合は以下の文章は読まなくていいです。


## 手順


### ターミナルでxrandrを実行

    $ xrandr

xrandrを実行するとこんな感じの画面が出ます。なお以下の出力はマルチディスプレイの設定をした後のものです。

    Screen 0: minimum 320 x 200, current 3286 x 1080, maximum 8192 x 8192
    LVDS connected primary 1366x768+1920+0 (normal left inverted right x axis y axis) 256mm x 144mm
       1366x768      59.97*+
       1280x720      59.97  
       1152x768      59.95  
       1024x768      59.95  
       800x600       59.96  
       848x480       59.94  
       720x480       59.94  
       640x480       59.94  
    HDMI-0 connected 1920x1080+0+0 (normal left inverted right x axis y axis) 600mm x 340mm
       1920x1080     60.00*   60.00    59.94    30.00    24.00    29.97    23.98  
       1920x1080i    60.00    59.94  
       1600x900      60.00  
       1280x1024     60.02  
       1280x800      59.91  
       1152x864      59.97  
       1280x720      60.00    59.94  
       1024x768      60.00  
       800x600       60.32  
       720x480       60.00    59.94  
       640x480       60.00    59.94  
    VGA-0 disconnected (normal left inverted right x axis y axis)

今回，HDMI接続しているモニタはPCの性能上フルHDまでしか認識されませんでした。


### [exwm Wiki](https://github.com/ch11ng/exwm/wiki#randr-multi-screen) を参考にinit.elに設定を記述します。

    (require 'exwm-randr)
    (setq exwm-randr-workspace-output-plist '(0 "VGA1"))
    (add-hook 'exwm-randr-screen-change-hook
              (lambda ()
                (start-process-shell-command
                 "xrandr" nil "xrandr --output LVDS --mode 1366x768 --pos 1920x0 --output HDMI-0 --mode 1920x1080 --pos 0x0")))
    (exwm-randr-enable)


#### スクリーンショット

![img](01.png)

参考: [ArchWiki: マルチディスプレイ](https://wiki.archlinux.jp/index.php/%25E3%2583%259E%25E3%2583%25AB%25E3%2583%2581%25E3%2583%2587%25E3%2582%25A3%25E3%2582%25B9%25E3%2583%2597%25E3%2583%25AC%25E3%2582%25A4)

