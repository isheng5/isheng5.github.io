---
layout: page
title: "Archive"
description: "听·说"
header-img: "/oalurqnz4.bkt.clouddn.com/orange.jpg"
putout: true
sitemap:
  priority: "0.5"
  changefreq: "daily"
  lastmod: 2016-07-15
---


<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
