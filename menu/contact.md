---
layout: page
title: Contact
permalink: /contact
---

If you are having any problems, any questions or suggestions, feel free to [tweet at me](https://twitter.com/intent/tweet?text=%40paululele), or [file a GitHub issue](https://github.com/lenpaul/lagrange/issues/new)


<div id="tags" class="d-flex flex-wrap mx-xl-2">
  {% assign tags = '' | split: '' %}
  {% for t in site.tags %}
    {% assign tags = tags | push: t[0] %}
  {% endfor %}

  {% assign sorted_tags = tags | sort_natural %}

  {% for t in sorted_tags %}
    <div>
      <a class="tag" href="{{ t | slugify | url_encode | prepend: '/tags/' | append: '/' | relative_url }}">
        {{ t -}}
        <span class="text-muted">{{ site.tags[t].size }}</span>
      </a>
    </div>
  {% endfor %}
</div>
