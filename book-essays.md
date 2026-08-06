---

title: "Book Essays"
permalink: /reception/criticism/book-essays/
layout: single
header:
  overlay_image: /assets/images/header.jpg  # header image

    
---
<!--
# Featured Essays
{% include feature_row id="feature_row" %}
-->

# Book Essays

*This section brings together introductions, forewords, prefaces, prologues, and afterwords written by poets, critics, scholars, and translators to accompany editions of Narlan Matos's books.*

{% assign items = site.data.reception
  | where: "type", "book-essay"
  | sort: "year"
  | reverse %}

{% for item in items %}

<p>

<strong>{{ item.title }}</strong>

{% if item.publication_id %}

{% assign book = site.data.publications
  | where: "publication_id", item.publication_id
  | first %}

<br>

For

{% if book and book.url %}
<a href="{{ book.url | relative_url }}">
<em>
{% if book.full_title %}
{{ book.full_title }}
{% elsif book.subtitle %}
{{ book.title }}: {{ book.subtitle }}
{% else %}
{{ book.title }}
{% endif %}
</em>
</a>

{% elsif book %}

<em>
{% if book.full_title %}
{{ book.full_title }}
{% elsif book.subtitle %}
{{ book.title }}: {{ book.subtitle }}
{% else %}
{{ book.title }}
{% endif %}
</em>

{% else %}

<em>{{ item.publication_id }}</em>

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