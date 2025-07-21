---
layout: page
title: Links
description: 
keywords: 
comments: true
menu: Links
permalink: /links/
---

这里收藏一些我个人认为比较多链接资源，也欢迎大家通过下面的评论反馈更多的优质AI资源

> AI资源

<ul>
{% for link in site.data.links %}
  {% if link.src == 'AIresource' %}
  <li><a href="{{ link.url }}" target="_blank">{{ link.name}}</a></li>
  {% endif %}
{% endfor %}
</ul>

> AI资讯

<ul>
{% for link in site.data.links %}
  {% if link.src == 'AIvideo' %}
  <li><a href="{{ link.url }}" target="_blank">{{ link.name}}</a></li>
  {% endif %}
{% endfor %}
</ul>

> 吉他

<ul>
{% for link in site.data.links %}
  {% if link.src == 'music' %}
  <li><a href="{{ link.url }}" target="_blank">{{ link.name}}</a></li>
  {% endif %}
{% endfor %}
</ul>
