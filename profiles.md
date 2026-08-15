---
title: "Narlan Matos"
layout: splash
permalink: /about/profiles/
header:
  overlay_image: /assets/images/header.jpg  # header image



---

*Profiles of Narlan Matos published in literary journals, cultural publications, and other venues offer a broader view of his life, work, and international literary career.
These pieces often combine biography, bibliography, critical commentary, interviews, and selections of poetry.*

{% assign profiles = site.data.reception | where: "type", "profile" %}

{% if profiles.size > 0 %}

{% for item in profiles %}
  <article class="archive__item">
    {% if item.title %}
      <h2 class="archive__item-title">
        {% if item.url %}
          <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
        {% else %}
          {{ item.title }}
        {% endif %}
      </h2>
    {% endif %}

    {% if item.author %}
      <p><strong>{{ item.author }}</strong></p>
    {% endif %}

    {% if item.publication %}
      <p><em>{{ item.publication }}</em>{% if item.date %}, {{ item.date }}{% endif %}</p>
    {% endif %}

    {% if item.description %}
      <p>{{ item.description }}</p>
    {% endif %}
  </article>
{% endfor %}

{% endif %}




