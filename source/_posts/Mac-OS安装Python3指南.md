---
title: Mac OS安装Python3整理
abbrlink: be5d852
date: 2021-03-26 21:26:38
updated:
tags:
---
&emsp;&emsp;Python 是一个高层次的结合了解释性、编译性、互动性和面向对象的脚本语言。

&emsp;&emsp;Python 的设计具有很强的可读性，相比其他语言经常使用英文关键字，其他语言的一些标点符号，它具有比其他语言更有特色语法结构。
<!-- more -->

+ Python 是一种解释型语言： 这意味着开发过程中没有了编译这个环节。类似于PHP和Perl语言。

+ Python 是交互式语言： 这意味着，您可以在一个 Python 提示符 >>> 后直接执行代码。

+ Python 是面向对象语言: 这意味着Python支持面向对象的风格或代码封装在对象的编程技术。

&emsp;&emsp;Python 是初学者的语言：Python 对初级程序员而言，是一种伟大的语言，它支持广泛的应用程序开发，从简单的文字处理到 WWW 浏览器再到游戏。

&emsp;&emsp;最新版本的Mac OS X，High Sierra， 自带Python 2.7。

&emsp;&emsp;您不必安装和配置即可直接使用Python 2。本教程用来说明Python 3的安装。

&emsp;&emsp;OS X自带的Python版本更适合用于学习而不是开发。因为版本与Python官网发布的 官方最新稳定版本 相比可能已经过时。


# Let`s do it

&emsp;&emsp;在正式安装之前，应先安装C编译器。最快的方式是运行 `xcode-select --install` 来安装Xcode命令行工具。 您也可以从Mac应用商店下载完全版的 [Xcode](http://developer.apple.com/xcode/)， 或者更轻巧的 [OSX-GCC-Installer](https://github.com/kennethreitz/osx-gcc-installer#readme) 。

{% note info %}
 注意
**如果**已经安装了Xcode，请不要再安装 OSX-GCC-Installer。两者结合可能会引发难以诊断的问题。
{% endnote %}

{% note info %}
 注意
**执行**Xcode的全新安装完成后，须在终端执行下述命令 xcode-select --install 来安装命令行工具。
{% endnote %}

## 安装Homebrew
&emsp;&emsp;尽管OS X系统附带了大量Unix工具，熟悉Linux系统的人员使用时会发现缺少一个重要的组件——合适的包管理工具， [Homebrew](http://brew.sh/) 正好填补了这个空缺。

&emsp;&emsp;[安装Homebrew](http://brew.sh/#install)只需打开 终端 或个人常用的终端模拟器并运行：

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
## 配置Homebrew
&emsp;&emsp;运行这段脚本将列出它会引起的改变，并在安装开始前提示您。 安装完成Homebrew后，需将其所在路径插入到 PATH 环境变量的最前面，即在您所登录用户的 ~/.profile 文件末尾加上这一行：

```
export PATH="/usr/local/opt/python/libexec/bin:$PATH"
```

&emsp;&emsp;如果您使用的是 OS X 10.12（Sierra）或者更旧的系统，请使用如下命令

```
export PATH=/usr/local/bin:/usr/local/sbin:$PATH
```
## 安装Python3
&emsp;&emsp;接下来可以开始安装Python 3：

```
brew install python
```

&emsp;&emsp;这将持续几分钟,然后，enjoy coding!

# Pip
Homebrew 会为您安装 `pip3` 

`pip3` 是Homebrew版Python 3的 `pip` 的别名。

# 使用Python 3
这个时候，在您系统上Python 2.7是可用的。[Homebrew 版本的Python 2](https://pythonguidecn.readthedocs.io/zh/latest/starting/install/osx.html#install-osx) 和Python 3都安装了。

```
python
```

在终端输入上面的命令，将打开通过HomeBrew安装的Python解释器。

```
python2
```

在终端输入上面的命令，将会打开使用Homebrew安装的Python 2解释器（如果有）。

```
python3
```

在终端输入上面的命令，将会打开使用Homebrew安装的Python 3解释器（如果有）。

如果Homebrew版的Python 2安装了，`pip2` 指向Python 2。 如果Homebrew版的Python 3安装了，pip 指向Python 3。

本指南的其余部分假定 python 指 Python 3。

```
# 我安装Python 3了吗？
python --version
Python 3.6.4 Success!
# If you still see 2.7 ensure in PATH /usr/local/bin/ takes pecedence over /usr/bin/
```

# Pipenv & 虚拟环境
下一步安装 Pipenv，然后就可以安装依赖关系并管理虚拟环境。

虚拟环境工具通过为不同项目创建专属的 Python 虚拟环境，以实现其依赖的库独立保存在不同的路径。 这解决了“项目X依赖于 1.x 版本，但项目 Y 需要 4.x”的难题，并且维持全局的 site-packages 目录干净、易管理。

举个例子，通过这个工具可以实现依赖 Django 1.10 的项目与依赖 Django 1.8 的项目共存。

所以，向前！~~[进入到 Pipenv & 虚拟环境](#)~~ 文档中！