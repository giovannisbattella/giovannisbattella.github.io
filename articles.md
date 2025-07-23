---
layout: page
title: Articles
permalink: /articles/
---

<amp-img width="600" height="300" layout="responsive" src="http://lorempixel.com/600/300/sports"></amp-img>

<ul>
  {% assign featured_posts = site.posts | where: "featured", true %}
  {% for post in featured_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span style="color: gray;"> – {{ post.date | date: "%B %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
