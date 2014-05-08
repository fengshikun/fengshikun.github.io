---
layout: post
title: "ubuntu安装搜狗拼音输入法"
date: 2014-05-08 09:26:35 +0800
comments: true
categories:Linux: 
---
##ubuntu安装sougou输入法
##1.卸载ibus输入法
	sudo apt-get remove ibus

##2.添加安装源
	vim /etc/apt/sources.list
 
在打开的sources.list中加入以下两行：

	deb http://ppa.launchpad.net/fcitx-team/nightly/ubuntu quantal main
	deb-src http://ppa.launchpad.net/fcitx-team/nightly/ubuntu quantal main
##3.更新源
	sudo apt-get update

##4.安装fcitx和fcitx-sunpinyin输入法（可以不安装）

    sudo apt-get install fcitx fcitx-config-gtk fcitx-sunpinyin

    sudo apt-get install fcitx fcitx-config-gtk fcitx-sogoupinyin

##5.安装码表

    sudo apt-get install fcitx-table-all 

*注意第4个步骤：在安装包`fcitx-sogoupinyin`时，可能会出现Unable to locate package fcitx-sogoupinyin的错误，可以到我的网盘(暂时只上传了x64)单独下载http://pan.baidu.com/s/1qW14nfQ,然后用dpkg -i命令安装*
