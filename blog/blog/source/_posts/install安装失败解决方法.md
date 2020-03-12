---
title: install安装失败解决方法
date: 2019-11-04 20:16:06
tags:
	- install
thumbnail: http://ww3.sinaimg.cn/large/7853084cgw1f7vueqesr5j21jk0uh446.jpg
categories:
	- 技术

---



<center>关于npm install失败的解决方法</center>

#### 1.授权执行
```bash
1.授权执行
sudo npm install
2.运行高权限用户
sudo npm install --unsafe-perm
3.安装某个模块
sudo npm i 模块名 --unsafe-perms
4.清除代理
npm config set proxy false
5.清除缓存
npm cache clean
```