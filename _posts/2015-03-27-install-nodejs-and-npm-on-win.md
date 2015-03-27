---
layout: default
title: 安装nodejs和NPM模块管理(windows平台)
forward: true
---

安装nodejs
==========

- 下载nodejs官方windows版程序, [下载地址](https://nodejs.org/download/)  
> .msi 和 .exe的唯一区别是 .exe需要自己添加环境变量. 我选择的是.exe, 复制到D:\nodejs目录, 并且将D:\nodejs添加到系统的环境变量
- 能够正常执行<code>node -v</code>, 则nodejs安装成功  


安装NPM
==========
- 下载NPM源码, [下载地址](https://github.com/npm/npm/tags)  
- 解压到D:\npmjs目录, 执行一下命令: 
<pre><code>
    D:\>cd npmjs
    D:\npmjs>node cli.js install -gf
</code></pre>  
- 能够正常执行<code>npm -v</code>, 则NPM安装成功  
- NPM安装完成后, 将D:\nodejs\node_modules添加到系统的环境变量**NODE_PATH**中

使用NPM安装nodejs的包(以express为例)
====================
- 执行一下命令:  
<pre><code>
    npm install -g express //安装最新版本的express, -g 标识以全局的形式安装包
    npm install -g express-generator  //安装express-generator, 这样才能使用express命令
    npm remove -g express //删除express
</code></pre>  

- 使用<code>npm -g ls</code>查看已经安装的包

* NPM的使用方法, 请参考[官网](http://npmjs.org/)  