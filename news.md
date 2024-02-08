---
layout: page
title: News
permalink: /news/
---


{% for item in site.data.news %}
<h2>{{ item.title }}</h2>
{% assign date = item.date | date: "%e" | split: "" %}
{% assign last_day_digit = date | last %}
{% case last_day_digit %}
  {% when "1" %}{% assign date_suffix = "st" %}
  {% when "2" %}{% assign date_suffix = "nd" %}
  {% when "3" %}{% assign date_suffix = "rd" %}
  {% else %}{% assign date_suffix = "th" %}
{% endcase %}
<p>{{ item.date | date: "%e" }}{{ date_suffix }} {{ item.date | date: "%b %Y" }}</p>
<p>{{ item.body | markdownify }}</p>
{% endfor %}
