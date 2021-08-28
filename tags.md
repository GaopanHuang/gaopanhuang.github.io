---
layout: page
title: "Tags"
description: "tags搜索"  
header-img: "img/green.jpg"  
---

## tag列表

<div id='tag_cloud'>
{% for tag in site.tags %}
  <a href="#{{ tag[0] }}" title="{{ tag[0] }}" rel="{{ tag[1].size }}"><u><fond color='pink'>{{ tag[0] }}</fond></u></a>
{% endfor %}
</div>

## 文章列表

<ul class="listing">
{% for tag in site.tags %}
  <li class="listing-seperator" id="{{ tag[0] }}">{{ tag[0] }}</li>
{% for post in tag[1] %}
  <li class="listing-item">
  <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
  <a href="{{ post.url }}" title="{{ post.title }}"><u><fond color='pink'>{{ post.title }}</fond></u></a>
  </li>
{% endfor %}
{% endfor %}
</ul>

<script src="/media/js/jquery.tagcloud.js" type="text/javascript" charset="utf-8"></script> 
<script language="javascript">
$.fn.tagcloud.defaults = {
    size: {start: 1, end: 1, unit: 'em'},
      color: {start: '#f8e0e6', end: '#ff3333'}
};

$(function () {
    $('#tag_cloud a').tagcloud();
});
</script>
