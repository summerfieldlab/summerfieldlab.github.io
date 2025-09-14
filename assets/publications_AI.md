---
layout: page
title: Publications (AI / society)
permalink: /publications_AI/
---

This is a selected list of publications focusses on sociotechnical AI research and AI safety. You can find a full listing of our work on [Google Scholar](https://scholar.google.com/citations?user=ymlcN9AAAAAJ&hl=en).


{% for year in site.data.publications_AI %}
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
