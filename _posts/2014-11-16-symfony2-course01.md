---
layout: default
title: Symfony2教程01 - 配置和安装Symfony2
---

> Symfony在2014-11-06发布了Symfony2.6.0 BETA1版本, 如果是用于练习的话, 我们可以下载最新版本. 如果是用于产品开发, 个人建议还是采用Symfony2.3, 因为这是一个长期支持的版本(LTS). 请看[Symfony2 Version Schedule](/images/symfony2-version-schedule.jpg), 通过图片我们知道2.3将会维护到2017-05. 所以这个教程也是基于2.3的.

安装Symfony2
============

在安装Symfony2之前, 首先需要安装[Composer](http://getcomposer.org/)(当然我们也可以直接下载包进行解压), Composer是一个PHP依赖包的管理工具. 详细的安装说明见[官网](https://getcomposer.org/download/).

在安装完Composer后, 我们就来安装Symfony, 一条命令搞定:
<pre><code>composer create-project symfony/framework-standard-edition ./ '2.3.*'</code></pre>

等到命令执行完成, 会需要你配置数据库和邮件的一些信息, 可以全部回车, 后面我们直接修改配置文件, 请看[symfony2-install-complete.jpg](/images/symfony2-install-complete.jpg).

完成后我们, 我们在项目文件夹下执行下面的命令, 检查我们的PHP配置是否符合要求, 根据命令结果修改你的配置:
<pre><code>php app/check.php</code></pre>

配置Symfony2
============
配置vhost, 指向项目的web目录. 我的配置如下:
<pre><code>
ServerAdmin john.mao@expacta.com.cn
DocumentRoot "D:\Project\symfony-course\web"
ServerName symfony.course
ErrorLog "logs/symfony.course-error.log"
CustomLog "logs/symfony.course-access.log" combined
</code></pre>

完成后, 我们访问 http://symfony.course/app_dev.php , 就可以看到欢迎信息, OK, 我们就已经安装和配置好了Symfony