---
title: "Biographical & Literary Profiles"
layout: splash
permalink: /about/profiles/
header:
  overlay_image: /assets/images/header.jpg  # header image



---

*Profiles of Narlan Matos published in literary journals, cultural publications, and other venues offer a broader view of his life, work, and international literary career.
These pieces often combine biography, bibliography, critical commentary, interviews, and selections of poetry.*

{% assign items = site.data.reception
  | where: "type", "profile"
  | sort: "year"
  | reverse %}

{% for item in items %}

<p><strong>{{ item.year }}</strong><br>

{%- if item.authors %}{{ item.authors }}.{% endif -%}
{%- if item.title %} “{{ item.title }}.”{% endif -%}
{%- if item.publication %} <em>{{ item.publication }}</em>{% endif -%}
{%- if item.volume %} {{ item.volume }}{% endif -%}
{%- if item.issue %}({{ item.issue }}){% endif -%}
{%- if item.pages %}, pp. {{ item.pages }}{% endif -%}

</p>

{% if item.description %}

<p>{{ item.description }}</p> {% endif %}

<p>

{% if item.url %}
<a href="{{ item.url }}" target="_blank" rel="noopener">Online version</a>
{% endif %}

{% if item.url and item.local_copy %}
  |  
{% endif %}

{% if item.local_copy %}
<a href="{{ item.local_copy | relative_url }}" target="_blank" rel="noopener">Archived copy</a>
{% endif %}

{% if item.worldcat_link %}
{% if item.url or item.local_copy %}  |  {% endif %}
<a href="{{ item.worldcat_link }}" target="_blank" rel="noopener">WorldCat</a>
{% endif %}

</p>

{% endfor %}

