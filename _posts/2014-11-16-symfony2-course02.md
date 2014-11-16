---
layout: default
title: Symfony2教程02 - 说明
---

Bundle
========
Symfony2中一个比较重要的概念就是Bundle. 个人理解, Bundle就类似Symfony1中的插件, 我们可以开发各种不同的Bundle: UserBundle, CmsBundle ... , 在开发新项目的时候, 只需要安装加载需要的Bundle即可, 减少重复开发.  

环境
========
Symfony2有3个环境, 分别是:  
dev  - 开发环境  
test - 测试环境  
prod - 生产环境  

目录结构
========
<pre><code>
symfony-course
    app               -> 项目配置文件, 缓存, 日志, 资源目录
        config        -> 配置文件目录
            config.yml
            config_dev.yml
            config_prod.yml
            config_test.yml
            parameters.yml    -> 在其他配置文件中, 都可以使用变量, 这个配置文件就是定义这些变量的值
            routing.yml
            routing_dev.yml
            security.yml
        AppKernel.php -> 项目核心文件, 注册Bundle, 加载配置文件
    bin
    src               -> 项目Bundle目录
    vendor            -> 第三方Bundle目录
    web
        app.php       -> prod环境引导文件
        app_dev.php   -> dev环境引导文件
</code></pre>