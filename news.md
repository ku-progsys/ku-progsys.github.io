---
layout: page
title : News
permalink: /news/
navbar: false
---

## News

<p>
{% assign news = site.news | sort: "date" | reverse %}
{% for info in news %}
<div class="news">
  <div class="news-date">
{% assign m = info.date | date: "%B" %}

{% case m %}
  {% when 'April' or 'May' or 'June' or 'July' %}{{ m }}
  {% when 'September' %} Sept
  {% else %}{{ info.date | date: "%b" }}
{% endcase %}
{{ info.date | date: ' %d, %Y' }}</div>
  <div class="news-matter">{{ info.content | markdownify }}</div>
</div>
{% endfor %}
</p>
