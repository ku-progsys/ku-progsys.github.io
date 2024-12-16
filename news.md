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
{{ info.date | date: "%b" }}
{{ info.date | date: ' %d, %Y' }}</div>
  <div class="news-matter">{{ info.content | markdownify }}</div>
</div>
{% endfor %}
</p>
