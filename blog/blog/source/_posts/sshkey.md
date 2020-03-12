---
title: mac系统如何生成SSH key与GitHub通信
date: 2020-03-12 14:26:12
tags: [SSH key, github]
thumbnail: https://ww1.yunjiexi.club/2019/11/10/77ed753afff82702ddf485f8fe3b09db.jpg
categories: [技术]

---

<!-- more -->

###  检查 SSH key 是否存在
在终端输入：
```
ls -al ~/.ssh
```

如果没有，终端显示如下：
```
No such file or directory
```
如果已经存在，则会显示 id_rsa 和 id_rsa.pub

### 生成新的 SSH key
在终端输入：
```
ssh-keygen -t rsa -C "your_email@example.com"
```
<font color="#f00">其中 your_email@example.com 为你在 GitHub 注册时的邮箱</font>

成功后终端显示如下：
```
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/xxx/.ssh/id_rsa):
```
提示你保存 .ssh/id_rsa 的路径，这里直接 enter

```
Created directory '/Users/xxx/.ssh'.
Enter passphrase (empty for no passphrase):
```

提示输入 passphrase，每次与 GitHub 通信都会要求输入 passphrase，以避免某些「失误」，建议输入
<font color="#f00">这里有个问题需要注意，那就是当你在这里输入密码，以后在连接gitHub去push代码的时候都需要输入密码，非常蛋疼，所以在这里最好直接回车过即可，不用输入密码。</font>

成功后终端显示：

```
Your identification has been saved in /Users/xxx/.ssh/id_rsa.
Your public key has been saved in /Users/xxx/.ssh/id_rsa.pub.
The key fingerprint is:
16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48 your_email@example.com
The key's randomart image is:（后面图形省略）
```

### 添加 key 到 SSH

```
ssh-add ~/.ssh/id_rsa
```

此时会要求输入 passphrase，输入步骤二中填的 passphrase
成功后，终端显示：

```
Identity added: /Users/xxx/.ssh/id_rsa (/Users/xxx/.ssh/id_rsa)
```

最后，在 /Users/xxx/.ssh/ 生成两个文件，id_rsa 和 id_rsa.pub
此时，SSH key 已经生成成功

### 添加 SSH key 到 GitHub

+ 复制 id_rsa.pub 中的所有内容
打开 id_rsa.pub，终端命令：

```
vim ~/.ssh/id_rsa.pub
```

手动复制以 ssh-rsa 到以 your_email@example.com 结尾的所有内容
或者直接输入命令复制 id_rsa.pub 中的所有内容，终端命令：

```
pbcopy < ~/.ssh/id_rsa.pub
```

+ 登录 GitHub

打开个人 Settings-->SSH keys-->Add SSH key
Title 随便写 "尽量填写所在地址如：办公位置、家等"

### 检测 SSH key

输入命令：
```
ssh git@github.com
```

此时会验证 SSH key 是否可以访问 GitHub
成功显示如下：

> Hi your_name! You've successfully authenticated, but GitHub does not provide shell access.Connection to github.com closed.

<font color="#f00">以上为提示内容，不过这里还是有一个需要注意的地方，如果没有上面的成功提示输出的话也不要害怕，我们可以先自己在本地建立一个gitHub仓库，然后进行push操作，如果push成功那么设置是成功的，如果push不上去的话再去检查。</font>
