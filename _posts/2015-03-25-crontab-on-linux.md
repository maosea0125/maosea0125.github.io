---
layout: default
title: 使用Liunx的crontab配置定时任务
forward: true
---

定时任务的解释
============

<pre><code>* * * * * php /home/httpd/html/rapidmanager/scripts/cronjobs/exportSubscribersForBcn.php</code></pre>

上面有5个星号, 分别代表不同的时间设置:
- 分钟(0 ~ 59)
- 小时(0 ~ 23)
- 月份中的第几天(1 ~ 31)
- 月份(1 ~ 12)
- 星期中的第几天(0 ~ 6)(0标识星期天)

如果使用星号, 则表示每.

例如上面的例子就表示执行<pre><code>php /home/httpd/html/rapidmanager/scripts/cronjobs/exportSubscribersForBcn.php</code></pre>
- 每分钟
- 每小时
- 月份中的每天
- 每月
- 星期中的每天

每周五的01:00:00执行:
<pre><code>0 1 * * 5 php /home/httpd/html/rapidmanager/scripts/cronjobs/exportSubscribersForBcn.php</code></pre>

工作日的01:00:00执行:
<pre><code>0 1 * * 1-5 php /home/httpd/html/rapidmanager/scripts/cronjobs/exportSubscribersForBcn.php</code></pre>

每10分钟执行一次:
<pre><code>0,10,20,30,40,50 * * * * php /home/httpd/html/rapidmanager/scripts/cronjobs/exportSubscribersForBcn.php</code></pre>
或者:
<pre><code>*/10 * * * * php /home/httpd/html/rapidmanager/scripts/cronjobs/exportSubscribersForBcn.php</code></pre>

[阅读原文](http://kvz.io/blog/2007/07/29/schedule-tasks-on-linux-using-crontab/)