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

## Original-Language (Portuguese) Anthologies

{% assign portuguese_anthologies = site.data.publications
| where: "collection", "anthologies"
| where: "publication_languages", "Portuguese"
| sort: "publication_date"
| reverse
%}

{% if portuguese_anthologies.size > 0 %}

{% for item in portuguese_anthologies %}

<p><strong>{{ item.publication_date }}</strong><br>

{%- if item.url -%}
<a href="{{ item.url | relative_url }}"><em>{{ item.full_title | default: item.title }}</em></a>
{%- else -%}
<em>{{ item.full_title | default: item.title }}</em>
{%- endif -%}

{%- if item.authors %} {{ item.authors }}.{% endif -%}
{%- if item.publication_place %} {{ item.publication_place }}.{% endif -%}
{%- if item.publisher %} {{ item.publisher }}.{% endif -%}
{%- if item.edition %} {{ item.edition }}.{% endif -%}
{%- if item.pages %} pp. {{ item.pages }}.{% endif -%}
{%- if item.isbn %} ISBN {{ item.isbn }}.{% endif -%}
{%- if item.worldcat_link %} · <a href="{{ item.worldcat_link }}" target="_blank" rel="noopener">WorldCat</a>{% endif -%}
{%- if item.read_link %} · <a href="{{ item.read_link }}" target="_blank" rel="noopener">Read</a>{% endif -%}

</p>

{% endfor %}

{% endif %}


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

## Periodical Publications
{% assign translated_periodicals = site.data.publications
| where: "collection", "periodicals"
| where_exp: "item", "publication_languages != 'Portuguese'"
| sort: "publication_date"
| reverse
%}

{% if translated_periodicals.size > 0 %}

{% for item in translated_periodicals %}

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

# Reception
## Reviews

{% assign reviews = site.data.reception
| where: "type", "review"
| sort: "year"
| reverse
%}

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

{% endif %}



## Critical Essays




## Academic Studies

{% assign academic = site.data.reception
| where: "type", "academic"
| sort: "year"
| reverse
%}

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

{% endif %}

## Book Essays

{% assign book_essays = site.data.reception
| where: "type", "book-essay"
| sort: "year"
| reverse
%}


{% assign book = site.data.publications
| where: "publication_id", item.publication_id
| first
%}

<p><strong>{{ item.year }}</strong><br>

{%- if item.authors %}{{ item.authors }}.{% endif -%}
{%- if item.title %} “{{ item.title }}.”{% endif -%}

{% if book %}
<br>
For
{% if book.url %}
<a href="{{ book.url | relative_url }}">
<em>{{ book.full_title | default: book.title }}</em>
</a>
{% else %}
<em>{{ book.full_title | default: book.title }}</em>
{% endif %}
{% endif %}

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

{% endif %}




{% comment %}

{% endcomment %}

{% assign introductions = site.data.reception
| where: "type", "introduction"
| sort: "year"
| reverse
%}

{% if introductions.size > 0 %}

<h2>Introductions, Forewords, Prefaces, Prologues &amp; Afterwords</h2>

{% for item in introductions %}

{% assign book = site.data.publications
| where: "publication_id", item.publication_id
| first
%}

<p><strong>{{ item.year }}</strong><br>

{%- if item.authors %}{{ item.authors }}.{% endif -%}
{%- if item.title %} “{{ item.title }}.”{% endif -%}

{% if book %}
<br>
For
{% if book.url %}
<a href="{{ book.url | relative_url }}">
<em>{{ book.full_title | default: book.title }}</em>
</a>
{% else %}
<em>{{ book.full_title | default: book.title }}</em>
{% endif %}
{% endif %}

{%- if item.publication %} <em>{{ item.publication }}</em>{% endif -%}
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
<a href="{{ item.local_copy | relative_url }}">Archived copy</a>
{% endif %}

{% if item.worldcat_link %}
{% if item.url or item.local_copy %}  |  {% endif %}
<a href="{{ item.worldcat_link }}" target="_blank" rel="noopener">WorldCat</a>
{% endif %}

</p>

{% endfor %}

{% endif %}

## Interviews
(coming soon!)
