---
layout: home
title: ""
permalink: /
author_profile: true
entries_layout: grid
paginate: 3
filter: tags
---
<h2>Filter by Tag</h2>

<div id="tag-filters">
  <button onclick="filterPosts('all')">All</button>
  {% assign tags = site.tags | sort %}
  {% for tag in tags %}
    <button onclick="filterPosts('{{ tag[0] }}')">{{ tag[0] }}</button>
  {% endfor %}
</div>

<hr>

<div id="posts-container">
  {% for post in paginator.posts %}
    <div class="post-item"
         data-tags="{% for tag in post.tags %}{{ tag }} {% endfor %}">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt }}</p>
      <small>
        Tags:
        {% for tag in post.tags %}
          <span>{{ tag }}</span>
        {% endfor %}
      </small>
    </div>
  {% endfor %}
</div>

<script>
function filterPosts(tag) {
  const posts = document.querySelectorAll('.post-item');

  posts.forEach(post => {
    if (tag === 'all') {
      post.style.display = 'block';
    } else {
      const tags = post.getAttribute('data-tags');
      post.style.display = tags.includes(tag) ? 'block' : 'none';
    }
    </script>
  });
}
</script>
