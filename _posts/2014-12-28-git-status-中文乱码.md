---
layout: post
title: "git status 中文乱码"
description: ""
category: 
tags: []
---

    $ git config --global core.quotepath false

refer [here](http://blog.crhan.com/2012/09/git-status-中文乱码解决/)

man *git-config*

> *core.quotepath*<br />
>
> The commands that output paths (e.g.  ls-files, diff), when not given the -z option, will quote "unusual" characters in the pathname by enclosing the pathname in a
> double-quote pair and with backslashes the same way strings in C source code are quoted. If this variable is set to false, the bytes higher than 0x80 are not quoted but output as verbatim. Note that double quote, backslash and control characters are always quoted without -z regardless of the setting of this variable.
