---
title: "Complete Bibliography"
layout: single
permalink: /about/bibliography/
header:
  overlay_image: /assets/images/header.jpg  # header image



---

*This bibliography provides a comprehensive record of Narlan Matos's published work, including books, poems, translations, anthologies, interviews, scholarly publications, and other literary contributions. Where available, entries link to records elsewhere on this site and to external or archived sources.*



# Books
## Original Poetry Collections

{% assign original_books = site.data.publications
| where: "collection", "books"
| where: "type", "original"
| sort: "publication_date"
| reverse
%}

{% for item in original_books %}

<p><strong>{{ item.publication_date }}</strong><br>

{%- if item.url -%}
<a href="{{ item.url | relative_url }}"><em>{{ item.full_title | default: item.title }}</em></a>
{%- else -%}
<em>{{ item.full_title | default: item.title }}</em>
{%- endif -%}

{%- if item.authors %} {{ item.authors }}.{% endif -%}
{%- if item.publication_place %} {{ item.publication_place }}.{% endif -%}
{%- if item.publisher %} {{ item.publisher }}:{% endif -%}
{%- if item.edition %} {{ item.edition }}.{% endif -%}
{%- if item.isbn %} ISBN {{ item.isbn }}.{% endif -%}
{%- if item.worldcat_link %} · <a href="{{ item.worldcat_link }}" target="_blank" rel="noopener">WorldCat</a>{% endif -%}

</p>

{% endfor %}


## Translated and Multilingual Editions

{% assign translated_books = site.data.publications
| where: "collection", "translations"
| sort: "publication_date"
| reverse
%}

{% if translated_books.size > 0 %}

{% for item in translated_books %}

<p><strong>{{ item.publication_date }}</strong><br>

{%- if item.url -%}
<a href="{{ item.url | relative_url }}"><em>{{ item.full_title | default: item.title }}</em></a>
{%- else -%}
<em>{{ item.full_title | default: item.title }}</em>
{%- endif -%}

{%- if item.authors %} {{ item.authors }}.{% endif -%}
{%- if item.translated_languages %} {{ item.translated_languages }}.{% endif -%}
{%- if item.translators %} Translated by {{ item.translators }}.{% endif -%}
{%- if item.publication_place %} {{ item.publication_place }}.{% endif -%}
{%- if item.publisher %} {{ item.publisher }}:{% endif -%}
{%- if item.edition %} {{ item.edition }}.{% endif -%}
{%- if item.isbn %} ISBN {{ item.isbn }}.{% endif -%}
{%- if item.worldcat_link %} · <a href="{{ item.worldcat_link }}" target="_blank" rel="noopener">WorldCat</a>{% endif -%}

</p>

{% endfor %}

{% endif %}