---
layout: page
title: "Archive"
description: "文章归档"
header-img: "img/green.jpg"
---


<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <h2 class="listing-seperator">{{ y }}</h2>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}"><u style="color:pink"><p style="color:pink">{{ post.title }}</p></u></a>
  </li>
{% endfor %}
</ul>
