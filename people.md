---
layout: page
title: People
permalink: /people/
---


{% for title in site.data.people %}
<h2>{{ title[0] }}</h2>
<ul>
  {% for person in title[1] %}
    <li><ul>
        <li><img src="{{ person.img }}" alt="{{ person.name }}"></li>
        <li><b>{{ person.name }}</b></li>
        <li>{{ person.bio | markdownify }}</li>
    </ul></li>
    {% endfor %}
</ul>
{% endfor %}
