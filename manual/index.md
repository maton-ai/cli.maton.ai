---
layout: default
title: Manual
permalink: /manual/
---

# Maton CLI manual

Reference for every `maton` command.

<ul class="manual-index">
{% assign pages = site.pages | where_exp: "p", "p.path contains 'manual/maton'" | sort: "path" %}
{% for p in pages %}
  <li><a href="{{ p.url | relative_url }}"><code>{{ p.path | remove: 'manual/' | remove: '.md' | replace: '_', ' ' }}</code></a></li>
{% endfor %}
</ul>
