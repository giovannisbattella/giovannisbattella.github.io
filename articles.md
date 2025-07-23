---
layout: page
title: Articles
permalink: /articles/
---

<amp-img width="600" height="300" layout="responsive" src="http://lorempixel.com/600/300/sports"></amp-img>

{% comment %}
  1.  Find all posts where 'featured: true' is set in the front matter.
  2.  The posts are automatically sorted by date, newest first.
{% endcomment %}
{% assign featured_posts = site.posts | where: "featured", true %}

{% comment %}
  Check if any featured posts were found before trying to loop.
{% endcomment %}
{% if featured_posts.size > 0 %}

  {% comment %}
    Loop through each post in the 'featured_posts' collection.
  {% endcomment %}
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
