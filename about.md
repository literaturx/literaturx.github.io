---
layout: default
title: About
---
# literaturx
It a project about literaturx

### Contributor
<ul>
  {% for author in site.authors %}
    <li>
      <b><a href="{{site.baseurl}}{{ author.url }}">{{ author.name }}</a></b>
			({{ author.position }})
    </li>
  {% endfor %}
</ul>