---
title: Categories
layout: page
---
<div id='tag_cloud'>{% for cat in site.categories %}<a href="#{{ cat[0] }}" title="{{ cat[0] }}" rel="{{ cat[1].size }}">{{ cat[0] }} ({{ cat[1].size }})</a>{% endfor %}</div>
<ul class="listing">{% for cat in site.categories %}
  <li class="listing-seperator" id="{{ cat[0] }}">{{ cat[0] }}</li>{% for post in cat[1] %}
  <li class="listing-item"><span class="time">{{ post.date | date:"%Y-%m-%d" }}</span><a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>{% endfor %}{% endfor %}
</ul>
<!-- <script src="/media/js/jquery.tagcloud.js" type="text/javascript" charset="utf-8"></script> 
<script type="text/javascript">
$.fn.tagcloud.defaults = {
    size: {start: 1, end: 1, unit: 'em'},
      color: {start: '#f8e0e6', end: '#ff3333'}
};
$(function () {
    $('#tag_cloud a').tagcloud();
});
</script> -->