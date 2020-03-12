---
title: markdown使用教程
date: 2019-11-04 20:14:49
tags:
	- markdown
thumbnail: http://ww3.sinaimg.cn/large/7853084cgw1f7vueqesr5j21jk0uh446.jpg
categories:
	- 技术

---

# <center>[markdown通用语法使用](https://wt812.github.io/) </center>

#### diff
```diff
+ 鸟宿池边树，僧敲月下门 
- 鸟宿池边树，僧推月下门
```

#### music
```
<audio id="audio" controls="" preload="none">
<source id="mp3" src="http://m8.music.126.net/20191103112212/4e752911a01696cdc8d3ffebf15b524d/ymusic/9f97/e40c/fb9d/be0f72b605a0c3d2ccbd6eaa7daa73e2.mp3">
</audio>
```
<audio id="audio" controls="" preload="none">
<source id="mp3" src="http://m8.music.126.net/20191103112212/4e752911a01696cdc8d3ffebf15b524d/ymusic/9f97/e40c/fb9d/be0f72b605a0c3d2ccbd6eaa7daa73e2.mp3">
</audio>


#### 复选框
```
- [x] 需求分析
- [x] 系统设计
- [x] 详细设计
- [ ] 编码
- [ ] 测试
- [ ] 交付
```
- [x] 需求分析
- [x] 系统设计
- [x] 详细设计
- [ ] 编码
- [ ] 测试
- [ ] 交付



#### 锚机
```
- [锚机测试](#锚机测试)
### <a id="锚机测试">锚机测试</a>
```
[锚机测试](#锚机测试)


#### 锚机2
```
<a href="#测试2">测试2</a>
|
|
|
|
<a id="测试2">测试2</a>
```
<a href="#测试2">锚点测试2</a>
|
|
|
|
<a id="测试2">看到了吗</a>


#### 大标题 小标题
```
大标题
===
小标题
---
```

大标题
===
小标题
---


#### 添加背景颜色
```
<table><tr><td bgcolor=yellow>背景色yellow</td></tr></table>
```
<table><tr><td bgcolor=yellow>背景色yellow</td></tr></table>

<a id="锚机测试">到这里了</a>
#### 上标
```
你好<sup>12</sup>
```
你好<sup>12</sup>


#### 下标
```
H<sub>2</sub>O  CO<sub>2</sub>
```
H<sub>2</sub>O  CO<sub>2</sub>


#### 定义文本字体颜色及字体字号、字体家族
```
<font color=#ff544b size=3 face="黑体">color=#0099ff size=3 face="黑体"</font>
```
<font color=#ff544b size=3 face="黑体">color=#0099ff size=3 face="黑体"</font>


#### 文本居中
```
<center>这一行需要居中</center>
```
<center>这一行需要居中</center>

#### javascript代码
```javascript
$(document).ready(function () {
    alert('wt');
});
```

#### 加粗 斜体 斜体加粗 删除线 下划线
```
*斜体文本*
_斜体文本_
**粗体文本**
__粗体文本__
***粗斜体文本***
___粗斜体文本___
~~这是加删除线的文字~~
<u>带下划线文本</u>
```
*斜体文本*
_斜体文本_
**粗体文本**
__粗体文本__
***粗斜体文本***
___粗斜体文本___
~~这是加删除线的文字~~
<u>带下划线文本</u>


#### 引用
```
>这是引用的内容
>>这是引用的内容
>>>>>>>>>>这是引用的内容
```
>这是引用的内容
>>这是引用的内容
>>>>>>>>>>这是引用的内容


#### 图片1
```
![图片alt](http://ww3.sinaimg.cn/large/7853084cgw1f7vueqesr5j21jk0uh446.jpg '图片title')
图片alt就是显示在图片下面的文字，相当于对图片内容的解释。
图片title是图片的标题，当鼠标移到图片上时显示的内容。title可加可不加
```
如：
![这是个图片](http://ww3.sinaimg.cn/large/7853084cgw1f7vueqesr5j21jk0uh446.jpg '测试图片')


#### 图片2
```
<img src="http://ww3.sinaimg.cn/large/7853084cgw1f7vueqesr5j21jk0uh446.jpg" width="50px">
```
<img src="http://ww3.sinaimg.cn/large/7853084cgw1f7vueqesr5j21jk0uh446.jpg" width="50px">


#### 高级图片链接
```
这个链接用 1 作为网址变量 [wt][1].

[1]: http://ww3.sinaimg.cn/large/7853084cgw1f7vueqesr5j21jk0uh446.jpg
```
这个链接用 1 作为网址变量 [图片地址].

[图片地址]: http://ww3.sinaimg.cn/large/7853084cgw1f7vueqesr5j21jk0uh446.jpg
注意：两段文字之间需要空格

#### 超链接1
```bash
[超链接名](https://wt812.githu.io "超链接title")
title可加可不加
```
[超链接名](https://wt812.githu.io "超链接title")
title可加可不加


#### 超链接2
```
<https://wt812.githu.io>
```
<https://wt812.githu.io>


#### 高级超链接
```
链接也可以用变量来代替，文档末尾附带变量地址：
这个链接用 1 作为网址变量 [wt][1]
这个链接用 wtblog 作为网址变量 [wt][wtblog]
然后在文档的结尾为变量赋值（网址）

  [1]: http://wt.github.io/
  [wt]: http://wt.github.io/
```
链接也可以用变量来代替，文档末尾附带变量地址：
这个链接用 1 作为网址变量 [wt][1]
这个链接用 wtblog 作为网址变量 [wt][wtblog]
然后在文档的结尾为变量赋值（网址）

  [1]: http://wt.github.io/
  [wtblog]: http://wt.github.io/


#### 列表
```bash
- 列表内容
+ 列表内容
* 列表内容
注意：- + * 跟内容之间都要有一个空格
```
- 列表内容
+ 列表内容
* 列表内容
注意：- + * 跟内容之间都要有一个空格


#### 有序列表
```bash
1. 列表内容
2. 列表内容
3. 列表内容
注意：序号跟内容之间要有空格
```
1. 列表内容
2. 列表内容
3. 列表内容
注意：序号跟内容之间要有空格


#### 列表嵌套
```
1. 第一项：
    - 第一项嵌套的第一个元素
    - 第一项嵌套的第二个元素
2. 第二项：
    - 第二项嵌套的第一个元素
    - 第二项嵌套的第二个元素
```

1. 第一项：
    - 第一项嵌套的第一个元素
    - 第一项嵌套的第二个元素
2. 第二项：
    - 第二项嵌套的第一个元素
    - 第二项嵌套的第二个元素


#### 列表中的引用
```
* 第一项
    > 菜鸟教程
    > 学的不仅是技术更是梦想
* 第二项
	> dsdsdsd
	> 大家看风景的看法
```
* 第一项
    > 菜鸟教程
    > 学的不仅是技术更是梦想
* 第二项
	> dsdsdsd
	> 大家看风景的看法


#### 表格
```bash
表头|表头|表头
---|:--:|---:
内容|内容|内容
内容|内容|内容
```
表头|表头|表头
---|:--:|---:
内容|内容|内容
内容|内容|内容

第二行分割表头和内容。
- 有一个就行，为了对齐，多加了几个
文字默认居左
-两边加：表示文字居中
-右边加：表示文字居右
注：原生的语法两边都要用 | 包起来。此处省略


#### 行内标签
```
`create database hero`
```
`create database hero`