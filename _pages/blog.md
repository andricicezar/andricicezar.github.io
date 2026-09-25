---
title: Blog
permalink: /blog/
published: false  # blog disabled for now
---

Older posts, written in Romanian.

<div class="entries">
{%- for post in site.posts %}
  <div class="entry">
    <div class="entry__venue">{{ post.date | date: '%b %Y' }}</div>
    <div class="entry__body"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></div>
  </div>
{%- endfor %}
</div>
