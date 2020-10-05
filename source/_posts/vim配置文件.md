---
title: vim配置文件
date: 2020-10-05 20:41:31
tags: vim
---



## 配置文件位置

当前登录用户的宿主目录下，比如root 用户就是/root/，文件为`.vimrc`



## 配置文件内容

```bash
#配置目录树快捷键F2启动
map <f2> :NERDTreeToggle<CR>

#配置默认目录
cd E:\phpStudy\WWW\

#配置编码
:set encoding=utf-8
:set fileencodings=ucs-bom,utf-8,cp936
:set fileencoding=gb2312
:set termencoding=utf-8

#解决菜单乱码
source $VIMRUNTIME/delmenu.vim
source $VIMRUNTIME/menu.vim

#解决consle提示信息输出乱码
language messages zh_CN.utf-8

#字体设置
:set guifont=Source_Code_Pro:h12:cANSI:qDRAFT
colo evening

#自动补全
autocmd InsertEnter * let save_cwd = getcwd() | set autochdir
autocmd InsertLeave * set noautochdir | execute 'cd' fnameescape(save_cwd)
set omnifunc=syntaxcomplete#Complete

#tab缩进4个空格
set smartindent  
set tabstop=4  
set shiftwidth=4  
set expandtab  
set softtabstop=4

#禁止保存后产生.un~文件
set noundofile
set nobackup
set noswapfile
```