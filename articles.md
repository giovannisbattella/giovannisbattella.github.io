---
layout: page
title: Articles
permalink: /articles/
---

<amp-img width="600" height="300" layout="responsive" src="http://lorempixel.com/600/300/sports"></amp-img>

<h1>Articles</h1>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span style="color: gray;"> – {{ post.date | date: "%B %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
