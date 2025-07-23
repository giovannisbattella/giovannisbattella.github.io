---
layout: page
title: Articles
permalink: /articles/
---

<amp-img width="600" height="300" layout="responsive" src="http://lorempixel.com/600/300/sports"></amp-img>

{% assign featured_posts = site.posts | where: "featured", true %}

{% if featured_posts.size > 0 %}

  {% for post in featured_posts %}
    <article>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt }}</p>
    </article>
    <hr>
  {% endfor %}

{% else %}

  <p>There are no featured articles to display.</p>

{% endif %}
