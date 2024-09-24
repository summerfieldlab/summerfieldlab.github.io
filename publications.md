---
layout: page
title: Publications
permalink: /publications/
---

This is a selected list of publications. You can find a full listing of our work on [Google Scholar](https://scholar.google.com/citations?user=ymlcN9AAAAAJ&hl=en).


{% for year in site.data.publications %}
<h2>{{ year[0] }}</h2>
<ul>
  {% for publication in year[1] %}
    <li><ul>
        {% if publication.paper_url and publication.paper_url != "" %}
            <li><a href="{{ publication.paper_url }}" target="_blank"><img src="{{ publication.img }}" alt="Publication image"></a></li>
        {% else %}
            <li><img src="{{ publication.img }}" alt="Publication image"></li>
        {% endif %}
        <li>{{ publication.title }}</li>
        <li>{{ publication.authors }}</li>
        <li>{{ publication.journal }}</li>
    </ul></li>
    {% endfor %}
</ul>
{% endfor %}
