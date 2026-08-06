---

title: "Introductions & Forewords"
permalink: /reception/criticism/introductions/
layout: single
header:
  overlay_image: /assets/images/header.jpg  # header image

    
---
<!--
# Featured Essays
{% include feature_row id="feature_row" %}
-->

# Introductions, Forewords, Prefaces, and Afterwords

{% assign items = site.data.reception
  | where: "type", "introduction"
  | sort: "year"
  | reverse %}

{% for item in items %}

<p>

<strong>{{ item.title }}</strong>

{% if item.related_work %}
<br>

{% if item.related_work_url %}
For
<a href="{{ item.related_work_url | relative_url }}">
<em>{{ item.related_work }}</em>
</a>
{% else %}
For <em>{{ item.related_work }}</em>
{% endif %}

{% endif %}

{% if item.authors %}
<br>
{{ item.authors }}
{% endif %}

{% if item.publication %}
<br>

<em>{{ item.publication }}</em>

{% if item.publication_place %}
, {{ item.publication_place }}
{% endif %}

{% if item.publisher %}
: {{ item.publisher }}
{% endif %}

{% if item.year %}
, {{ item.year }}
{% endif %}

{% endif %}

{% if item.language %}
<br>
({{ item.language }})
{% endif %}

</p>

{% if item.description %}
<p>{{ item.description }}</p>
{% endif %}

{% if item.url or item.local_copy %}
<p>

{% if item.url %}
<a href="{{ item.url }}" target="_blank" rel="noopener">
Online version
</a>
{% endif %}

{% if item.url and item.local_copy %}
&nbsp; | &nbsp;
{% endif %}

{% if item.local_copy %}
<a href="{{ item.local_copy | relative_url }}"
   target="_blank"
   rel="noopener">
Archived copy
</a>
{% endif %}

</p>
{% endif %}

<hr>

{% endfor %}