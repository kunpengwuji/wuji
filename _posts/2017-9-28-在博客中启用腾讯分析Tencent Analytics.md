---
title: �ڲ�����������Ѷ����Tencent Analytics
date: 2017-09-29T07:30:28.000Z
categories:
  - Tech
tags:
  - ��Ѷ
  - ����
  - �̳�
published: false
---

��ǰһƪ���������Ǵ�����һ������GitHub�йܷ���Ĳ��ͣ���������ʹ����Ѷ����վ��������Tencent Analytics�����ò��͵�ͳ�Ʒ�����


## ע��Tencent Analytics
TA��ַ��http://ta.qq.com/ 
- ֱ��ʹ��QQ��ע�ἴ��
- ע����ʹ��QQ�ŵ�¼

## ��ȡTA����
- ���һ������վ��
- ����վ���б������Ӧվ��ġ���ȡ���롱
- �õ����´���
```
<script type="text/javascript" src="http://tajs.qq.com/stats?sId=XXXXXXXX" charset="UTF-8"></script>
```
- ���С�SId=�������һ�����ּ�Ϊ���TA ID

## ����TA
- �޸Ĳ��͸�Ŀ¼�µ�config.yml�ļ���..\_config.yml�����ҵ�Tencent analytics ID�����������ȡ�õ�����
``` 
# Tencent analytics ID
tencent_analytics: XXXXXXXX
```
  
- �鿴tencent-analytics.html�ļ���..\_includes\_third-party\analytics\tencent-analytics.html���������޸ģ�ֻ��ȷ�ϸ��ļ��а�����������TA���뼴�ɡ�
```
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

## ����
- �����ĺõ����ݷ�����GitHub��ʵ����TA�ڲ����е����ã�������ʱ��¼TA�鿴ͳ�Ʒ�������ˡ�
- TA��վ���б��е�����״̬���ܻ���ʾ���޷���ȡ����δ��⵽���롱�������������ͨ��JS���ð�װ���룬��ʾ��δ��⵽���롱�Լ���վ��������ǽ���������ʾ���޷���ȡ���������������󣬲�Ӱ������ͳ�ơ�

����޷�������Ѷ�����Ļ��������Գ���ʹ����������������������վ���������ٶȷ����ȣ������������������ƣ�ֻ���ȡ��Ӧ����ID������config.yml�ļ����ɡ�