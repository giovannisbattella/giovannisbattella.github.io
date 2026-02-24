---
title: "Explore Topics"
layout: archive
permalink: /explore/
author_profile: true
---

## Browse by Topic

{% assign tags = site.tags | sort %}

<div class="taxonomy__index">
{% for tag in tags %}
  <a href="{{ '/tags/#' | append: tag[0] | slugify | relative_url }}" class="taxonomy__item">
    {{ tag[0] }} ({{ tag[1].size }})
  </a>
{% endfor %}
</div>
