---
layout: post
title: Vim tricks that I never bothered to learn til now
---
If you have auto-indent turned on in .vimrc, and paste in code, it will add tabs to each line. You can temporarily ignore this with :set paste, but then you must set :set nopaste or suddenly my jk mappings (using jk vs esc to switch modes) will not work.
You can more easily avoid this morass by using '"+p' to paste into vim.
-----
