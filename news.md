---
layout: page
title: News
permalink: /news/
---


{% for item in site.data.news %}
<h2>{{ item.title }}</h2>
{% assign day = item.date | date: "%-d" %}
{% case day %}
  {% when "1" or "21" or "31" %}{% assign date_suffix = "st" %}
  {% when "2" or "22" %}{% assign date_suffix = "nd" %}
  {% when "3" or "23" %}{% assign date_suffix = "rd" %}
  {% else %}{% assign date_suffix = "th" %}
{% endcase %}
<p class="date">{{ day }}{{ date_suffix }} {{ item.date | date: "%b %Y" }}</p>
<p>{{ item.body | markdownify }}</p>
{% endfor %}
