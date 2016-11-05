---
layout: blogoldal
title: Blog
search_omit: true
redirect_from: "/hu/blog/"
---
<h2>Legfrissebb</h2>
<ul class="post-list">
{% for post in site.categories.blog limit:8 %}
  <li><article><a href="{{ site.url }}{{ post.url }}" style="color:#ca3333"> {{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y. %B %d." }}</time></span></a><a href="{{ site.url }}{{ post.url }}" style="text-decoration:none; color:#222">{% if post.excerpt %} <span class="excerpt">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
