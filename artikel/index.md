---
layout: page
title: Alles zum Thema Sirup.
excerpt: "An archive of articles sorted by date."
search_omit: true
---
<h2>Sirup herstellen, Sirup geniessen und mit Sirup kochen.</h2>
<ul class="post-list">
{% for post in site.categories.artikel %}
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d. %m. %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
