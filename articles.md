---
layout: page
title: Articles
permalink: /articles/
---

<amp-img width="600" height="300" layout="responsive" src="http://lorempixel.com/600/300/sports"></amp-img>

{% assign featured_post = site.posts | where: "featured", true | first %}
{% if featured_post %}
  <h2><a href="{{ featured_post.url | relative_url }}">{{ featured_post.title }}</a></h2>
  <p>{{ featured_post.excerpt }}</p>
{% endif %}
