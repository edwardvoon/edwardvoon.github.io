---
title: 设置python默认版本(MAC)
abbrlink: 4a17b156
---

&emsp;&emsp;回到之前我们遇到的问题，在终端输入`python --version`返回的版本是2.x.x。原因是，在mac系统下，就已经安装了python。我们该怎样在终端设置默认的python启动版本，也就是我们已经安装的python3。下面的设置，让你如愿以偿。
# 打开终端
输入命令
`open ~/.bash_profile`

返回的信息如果是

The file /Users/<电脑名>/.bash_profile does not exist.

意思是，`.bash_profile`不存在，那就看你是不是安装了`oh-my-zsh`,如果是，请接着往下看：

open ~/.zshrc