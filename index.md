---
layout: default
---

{% include overview.md %}

### News

<p>
{% assign news = site.news | sort: "date" | reverse %}
{% for info in news limit: 5 %}
<div class="news">
  <div class="news-date">
{{ info.date | date: "%b" }}
{{ info.date | date: ' %d, %Y' }}</div>
  <div class="news-matter">{{ info.content | markdownify }}</div>
</div>
{% endfor %}
</p>

[[More ...]({{site.baseurl}}/news/)]

## Projects

{% include projects.md %}

## People

<div class="people">
{% assign faculties = site.people | where: "type", "faculty" | sort: "last_name" %}
{% for person in faculties %}

<div class="person" id="{{person.relative_path}}">
  <img class="pp" src="{{ person.picture | prepend: site.baseurl }}">
  <h4 class="no-bottom">{{person.name}}</h4>
  <div class="since">Faculty<br/>
  <!-- {{person.started}} - Present -->
  </div>

  {{person.content | markdownify}}

  <div class="social">
  {% if person.webpage %}
  <a href="{{person.webpage}}" target="_blank"><i class="icon fa fa-globe"></i>Web</a><br>
  {% endif %}

  {% if person.email %}
  <a href="mailto:{{person.email}}"><i class="icon fa fa-envelope"></i>{{person.email}}</a><br>
  {% endif %}

  {% if person.twitter %}
  <a href="https://twitter.com/{{person.twitter}}" target="_blank"><i class="icon fa fa-twitter"></i>@{{person.twitter}}</a><br>
  {% endif %}
  </div>
</div>
{% endfor %}

{% assign students = site.people | where: "type", "phd" | sort: "last_name" %}
{% for person in students %}

<div class="person" id="{{person.relative_path}}">
  <img class="pp" src="{{ person.picture | prepend: site.baseurl }}">
  <h4 class="no-bottom">{{person.name}}</h4>
  <div class="since">Ph.D.<br/>
  <!-- {{person.started}} - Present -->
  </div>

  {{person.content | markdownify}}

  <div class="social">
  {% if person.webpage %}
  <a href="{{person.webpage}}" target="_blank"><i class="icon fa fa-globe"></i>Web</a><br>
  {% endif %}

  {% if person.email %}
  <a href="mailto:{{person.email}}"><i class="icon fa fa-envelope"></i>{{person.email}}</a><br>
  {% endif %}

  {% if person.twitter %}
  <a href="https://twitter.com/{{person.twitter}}" target="_blank"><i class="icon fa fa-twitter"></i>@{{person.twitter}}</a><br>
  {% endif %}
  </div>
</div>
{% endfor %}

{% assign students = site.people | where: "type", "ms" | sort: "last_name" %}
{% for person in students %}

<div class="person" id="{{person.relative_path}}">
  <img class="pp" src="{{ person.picture | prepend: site.baseurl }}">
  <h4 class="no-bottom">{{person.name}}</h4>
  <div class="since">Masters<br/>
  <!-- {{person.started}} - Present -->
  </div>

  {{person.content | markdownify}}

  <div class="social">
  {% if person.webpage %}
  <a href="{{person.webpage}}" target="_blank"><i class="icon fa fa-globe"></i>Web</a><br>
  {% endif %}

  {% if person.email %}
  <a href="mailto:{{person.email}}"><i class="icon fa fa-envelope"></i>{{person.email}}</a><br>
  {% endif %}

  {% if person.twitter %}
  <a href="https://twitter.com/{{person.twitter}}" target="_blank"><i class="icon fa fa-twitter"></i>@{{person.twitter}}</a><br>
  {% endif %}
  </div>
</div>
{% endfor %}

{% assign students = site.people | where: "type", "bs" | sort: "last_name" %}
{% for person in students %}

<div class="person" id="{{person.relative_path}}">
  <img class="pp" src="{{ person.picture | prepend: site.baseurl }}">
  <h4 class="no-bottom">{{person.name}}</h4>
  <div class="since">Undergraduate<br/>
  <!-- {{person.started}} - Present -->
  </div>

  {{person.content | markdownify}}

  <div class="social">
  {% if person.webpage %}
  <a href="{{person.webpage}}" target="_blank"><i class="icon fa fa-globe"></i>Web</a><br>
  {% endif %}

  {% if person.email %}
  <a href="mailto:{{person.email}}"><i class="icon fa fa-envelope"></i>{{person.email}}</a><br>
  {% endif %}

  {% if person.twitter %}
  <a href="https://twitter.com/{{person.twitter}}" target="_blank"><i class="icon fa fa-twitter"></i>@{{person.twitter}}</a><br>
  {% endif %}
  </div>
</div>
{% endfor %}

</div>

## Publications

{% assign pubs = site.data.publications | sort: "year" %}
{% for pub in pubs reversed %}

**[{{pub.title}}]({{pub.url}})**<br/>
{{pub.authors}}<br/>
_{{pub.venue}}_

{% endfor %}
