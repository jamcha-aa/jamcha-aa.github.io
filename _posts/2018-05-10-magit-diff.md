---
layout: post
title: 文章のどこが変更されたのかMagitで視覚化する
tags: [Emacs, Magit]
---

-   <http://www.clear-code.com/blog/2012/4/3.html> を参考に，init.elに以下の内容を追加します。
    
        ;; 文字単位での変更箇所は色を反転して強調
        (set-face-attribute 'diff-refine-changed nil
                        :foreground nil :background nil
                        :weight 'bold :inverse-video t)
        
        ;; diffを表示したらすぐに文字単位での強調表示も行う
        (defun diff-mode-refine-automatically ()
          (diff-auto-refine-mode t))
        (add-hook 'diff-mode-hook 'diff-mode-refine-automatically)
        
        ;; diffを表示しているときに文字単位での変更箇所も強調表示する
        ;; 'allではなくtにすると現在選択中のhunkのみ強調表示する
        (setq magit-diff-refine-hunk 'all)

-   例: 
    
    ![img](01.png)

-   あとがき
    
    通常，Magit (Gitも含む) では行単位でしか変更内容を表示しません。この設定を利用すると変更箇所を細かい部分まで確認でき，文章の編集に役立ちます。なおMagitを使わずにGitのみを利用する場合はこちらの記事を参考にしてください <https://qiita.com/skoji/items/28f1d6582cf81638cd3f>
