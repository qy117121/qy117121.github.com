---
title: Stay Hungry,Stay Foolish
layout: page
---

<ul class="listing">
 {% for post in paginator.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
<object classid='clsid:D27CDB6E-AE6D-11cf-96B8-444553540000' width='400' height='95' id='bdmp3widget3145'><param name='movie' value='http://box.baidu.com/widget/flash/mbsong.swf?name=stories&artist=hitomi'></param><param name='wmode' value='opaque'></param><param name='allowscriptaccess' value='always'></param><embed src='http://box.baidu.com/widget/flash/mbsong.swf?name=stories&artist=hitomi' type='application/x-shockwave-flash' wmode='opaque' allowscriptaccess='always' width='400' height='95' name='bdmp3widget3145'></embed></object>
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>

 {% if paginator.previous_page %}
  	{% if paginator.page == 2 %}
  		<a href="/" rel="bookmark"> << Previous Page</a>
  	{% else %}
  		<a href="/page{{ paginator.previous_page }}" rel="bookmark"> << Previous Page</a>
  	{% endif %}
  {% endif %}
  {% if paginator.next_page %}
  	<a href="/page{{ paginator.next_page }}" rel="bookmark" style="float:right">Next Page >></a>
  {% endif %}
