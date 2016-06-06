---
title: Crew
layout: page
---
<ul class="people-list">
{% for person_hash in site.data.people %}
{% assign person = person_hash[1] %}
{% assign person_url = site.baseurl | append: "/crew/" | append: person_hash[0] %}
  <li>
    {% if person.avatar %}
      <a href="{{ person_url }}">
        <img class="avatar" src="{{ person.avatar | prepend: site.baseurl }}" alt="{{ person.name }}">
      </a>
    {% endif %}
    <a href="{{ person_url }}">{{ person.name }}</a>
    {% if person.title %}
    <br><span class="person-title">{{ person.title }}</span>
    {% endif %}
  </li>
{% endfor %}
</ul>
