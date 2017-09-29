---
title: 在博客中启用腾讯分析Tencent Analytics
date: 2017-09-29T08:17:28.000Z
categories:
  - Tech
tags:
  - 腾讯
  - 博客
  - 教程
published: false
---

在前一篇文章中我们创建了一个基于GitHub托管服务的博客，现在我们使用腾讯的网站分析工具Tencent Analytics并启用博客的统计分析。


## 注册Tencent Analytics
TA网址：http://ta.qq.com/ 
- 直接使用QQ号注册即可
- 注册后可使用QQ号登录
![20170928_1_Tencent Analytics.jpg](https://raw.githubusercontent.com/kunpengwuji/wuji/master/_posts/20170928_1_Tencent Analytics.jpg)

## 获取TA代码
- 添加一个或多个站点
- 进入站点列表，点击对应站点的“获取代码”
- 得到如下代码
```Javascript
<script type="text/javascript" src="http://tajs.qq.com/stats?sId=XXXXXXXX" charset="UTF-8"></script>
```
- 其中“SId=”后面的一串数字即为你的TA ID
![20170928_2_TA Script.jpg](https://raw.githubusercontent.com/kunpengwuji/wuji/master/_posts/20170928_2_TA Script.jpg)

## 启用TA
- 修改博客根目录下的config.yml文件（..\_config.yml），找到Tencent analytics ID，并添加上面取得的数字
```Yaml 
# Tencent analytics ID
tencent_analytics: XXXXXXXX
```
  
- 查看tencent-analytics.html文件（..\_includes\_third-party\analytics\tencent-analytics.html），不用修改，只需确认该文件中包含了完整的TA代码即可。
```HTML
{% if site.tencent_analytics %}
  <script type="text/javascript">
    (function() {
      var hm = document.createElement("script");
      hm.src = "//tajs.qq.com/stats?sId={{ site.tencent_analytics }}";
      var s = document.getElementsByTagName("script")[0];
      s.parentNode.insertBefore(hm, s);
    })();
  </script>
{% endif %}
```

## 发布
- 将更改好的内容发布到GitHub就实现了TA在博客中的启用，可以随时登录TA查看统计分析结果了。
- TA的站点列表中的运行状态可能还显示“无法获取”或“未检测到代码”，这可能是由于通过JS调用安装代码，提示“未检测到代码”以及网站开启防火墙类软件，提示“无法获取”均属于正常现象，不影响数据统计。

如果无法启用腾讯分析的话，还可以尝试使用其它第三方分析服务，如站长分析、百度分析等，方法与上述过程类似，只需获取相应服务ID并调整config.yml文件即可。
