---
layout: post
title: "Emacs note"
description: ""
category: 
tags: []
---


### install 

* brew install with cocl and srgb
<http://www.emacswiki.org/emacs/EmacsForMacOS>

### configuraton

* scroll-bar,   (scroll-bar-mode -1) or M-x toggle-

* `M-x describe-font`  to see the font current


    (add-to-list 'default-frame-alist '(width  . 90))
    (add-to-list 'default-frame-alist '(height . 40))
    (add-to-list 'default-frame-alist '(font . "Source Code Pro for Powerline-12" ))

* theme , M-x load-theme
    (setq theme-default 'adwaita)')

* `M-x eval-buffer`

* emacs in terminal with 256 color

    `TERM=xterm-256color emacs -nw`

* el-get

