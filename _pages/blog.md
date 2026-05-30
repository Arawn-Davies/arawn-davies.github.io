---
title: Blog
layout: page
nav_order: 4
has_children: true
permalink: /blog
---

# Blog

Occasional posts on projects, music, gaming, Z80-based microcomputers, Amiga, PC and anything I find interesting.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span class="text-grey-dk-000"> &middot; {{ post.date | date: "%b %-d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
