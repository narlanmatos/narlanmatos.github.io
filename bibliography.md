---
title: "Complete Bibliography"
layout: single
permalink: /about/bibliography/
header:
  overlay_image: /assets/images/header.jpg  # header image



---

*This bibliography provides a comprehensive record of Narlan Matos's published work, including books, poems, translations, anthologies, interviews, scholarly publications, and other literary contributions. Where available, entries link to records elsewhere on this site and to external or archived sources.*


{% comment %}
==================================================
I. BOOKS
==================================================
{% endcomment %}

# Books

{% assign books = site.data.publications
  | where: "collection", "books"
%}

{% assign original_books = books
  | where_exp: "item", "item.type == 'original'"
  | sort: "publication_date"
  | reverse
%}

{% if original_books.size > 0 %}

## Poetry Collections

{% for item in original_books %}

<p>
<strong>{{ item.publication_date }}</strong><br>

{% if item.url %}
<a href="{{ item.url | relative_url }}">
<em>
{% if item.full_title %}
{{ item.full_title }}
{% elsif item.subtitle %}
{{ item.title }}: {{ item.subtitle }}
{% else %}
{{ item.title }}
{% endif %}
</em>
</a>
{% else %}
<em>
{% if item.full_title %}
{{ item.full_title }}
{% elsif item.subtitle %}
{{ item.title }}: {{ item.subtitle }}
{% else %}
{{ item.title }}
{% endif %}
</em>
{% endif %}

{% if item.publication_place %}
. {{ item.publication_place }}
{% endif %}

{% if item.publisher %}
: {{ item.publisher }}
{% endif %}

{% if item.worldcat_link %}
 · <a href="{{ item.worldcat_link }}" target="_blank" rel="noopener">WorldCat</a>
{% endif %}

</p>

{% endfor %}

{% endif %}


{% comment %}
==================================================
TRANSLATED BOOKS
==================================================
{% endcomment %}

{% assign translated_books = books
  | where_exp: "item", "item.type == 'translation'"
  | sort: "publication_date"
  | reverse
%}

{% if translated_books.size > 0 %}

## Translated and Multilingual Editions

{% for item in translated_books %}

<p>
<strong>{{ item.publication_date }}</strong><br>

{% if item.url %}
<a href="{{ item.url | relative_url }}">
<em>
{% if item.full_title %}
{{ item.full_title }}
{% elsif item.subtitle %}
{{ item.title }}: {{ item.subtitle }}
{% else %}
{{ item.title }}
{% endif %}
</em>
</a>
{% else %}
<em>
{% if item.full_title %}
{{ item.full_title }}
{% elsif item.subtitle %}
{{ item.title }}: {{ item.subtitle }}
{% else %}
{{ item.title }}
{% endif %}
</em>
{% endif %}

{% if item.translated_languages %}
. {{ item.translated_languages }}
{% endif %}

{% if item.translators %}
. Translated by {{ item.translators }}
{% endif %}

{% if item.publication_place %}
. {{ item.publication_place }}
{% endif %}

{% if item.publisher %}
: {{ item.publisher }}
{% endif %}

{% if item.worldcat_link %}
 · <a href="{{ item.worldcat_link }}" target="_blank" rel="noopener">WorldCat</a>
{% endif %}

</p>

{% endfor %}

{% endif %}



{% comment %}
==================================================
II. POEMS IN ANTHOLOGIES AND PERIODICALS
==================================================
==================================================
Uses publications that are not books and connects
them to poems through first/additional publication IDs.
==================================================
{% endcomment %}

# Poems in Anthologies and Periodicals

{% assign poem_publications = site.data.publications
  | where_exp: "item", "item.collection == 'anthologies' or item.collection == 'periodicals'"
  | sort: "publication_date"
  | reverse
%}

{% for publication in poem_publications %}

{% assign publication_poems = "" | split: "" %}

{% for poem in site.data.poems %}

{% assign poem_matches = false %}

{% if poem.first_publication_id == publication.publication_id %}
  {% assign poem_matches = true %}
{% endif %}

{% unless poem_matches %}

{% if poem.additional_publication_ids %}

{% assign additional_ids = poem.additional_publication_ids | split: ";" %}

{% for id in additional_ids %}

{% if id | strip == publication.publication_id %}
  {% assign poem_matches = true %}
  {% break %}
{% endif %}

{% endfor %}

{% endif %}

{% endunless %}

{% if poem_matches %}
  {% assign publication_poems = publication_poems | push: poem %}
{% endif %}

{% endfor %}


{% if publication_poems.size > 0 %}

{% assign publication_year = publication.publication_date %}

<p>

<strong>{{ publication_year }}</strong><br>

{% if publication.url %}
<a href="{{ publication.url | relative_url }}">
<em>{{ publication.title }}</em>
</a>
{% else %}
<em>{{ publication.title }}</em>
{% endif %}

{% if publication.publisher %}
. {{ publication.publisher }}
{% endif %}

{% if publication.publication_place %}
. {{ publication.publication_place }}
{% endif %}

{% if publication.worldcat_link %}
 · <a href="{{ publication.worldcat_link }}" target="_blank" rel="noopener">WorldCat</a>
{% endif %}

<br>

Poems by Narlan Matos:

{% for poem in publication_poems | sort: "title" %}

<a href="{{ '/poetry/poems/' | append: poem.poem_id | relative_url }}">
“{{ poem.title }}”
</a>{% unless forloop.last %}; {% endunless %}

{% endfor %}

</p>

{% endif %}

{% endfor %}



{% comment %}
==================================================
III. CRITICAL WRITING ABOUT NARLAN
==================================================
==================================================
REVIEWS
==================================================
{% endcomment %}

# Critical Writing About Narlan

## Reviews

{% assign reviews = site.data.reception
  | where: "type", "review"
  | sort: "year"
  | reverse
%}

{% for item in reviews %}

<p>

<strong>{{ item.year }}</strong><br>

{% if item.authors %}
{{ item.authors }}.
{% endif %}

{% if item.title %}
“{{ item.title }}.”
{% endif %}

{% if item.publication %}
<em>{{ item.publication }}</em>
{% endif %}

{% if item.publication_place %}
, {{ item.publication_place }}
{% endif %}

{% if item.publisher %}
: {{ item.publisher }}
{% endif %}

{% if item.publication_id %}

{% assign book = site.data.publications
  | where: "publication_id", item.publication_id
  | first %}

{% if book %}

<br>
On
{% if book.url %}
<a href="{{ book.url | relative_url }}">
<em>{{ book.full_title | default: book.title }}</em>
</a>
{% else %}
<em>{{ book.full_title | default: book.title }}</em>
{% endif %}

{% endif %}

{% endif %}

</p>

{% if item.url or item.local_copy %}

<p>

{% if item.url %}
<a href="{{ item.url }}" target="_blank" rel="noopener">Online version</a>
{% endif %}

{% if item.url and item.local_copy %}
&nbsp; | &nbsp;
{% endif %}

{% if item.local_copy %}
<a href="{{ item.local_copy | relative_url }}" target="_blank" rel="noopener">
Archived copy
</a>
{% endif %}

</p>

{% endif %}

{% endfor %}



{% comment %}
==================================================
CRITICAL ESSAYS
==================================================
{% endcomment %}

## Critical Essays

{% assign essays = site.data.reception
  | where: "type", "critical-essay"
  | sort: "year"
  | reverse
%}

{% for item in essays %}

<p>

<strong>{{ item.year }}</strong><br>

{% if item.authors %}
{{ item.authors }}.
{% endif %}

{% if item.title %}
“{{ item.title }}.”
{% endif %}

{% if item.publication %}
<em>{{ item.publication }}</em>
{% endif %}

{% if item.publication_place %}
, {{ item.publication_place }}
{% endif %}

{% if item.publisher %}
: {{ item.publisher }}
{% endif %}

</p>

{% if item.url or item.local_copy %}

<p>

{% if item.url %}
<a href="{{ item.url }}" target="_blank" rel="noopener">Online version</a>
{% endif %}

{% if item.url and item.local_copy %}
&nbsp; | &nbsp;
{% endif %}

{% if item.local_copy %}
<a href="{{ item.local_copy | relative_url }}" target="_blank" rel="noopener">
Archived copy
</a>
{% endif %}

</p>

{% endif %}

{% endfor %}



{% comment %}
==================================================
BOOK ESSAYS
==================================================
{% endcomment %}

## Book Essays

{% assign book_essays = site.data.reception
  | where: "type", "book-essay"
  | sort: "year"
  | reverse
%}

{% for item in book_essays %}

{% assign book = site.data.publications
  | where: "publication_id", item.publication_id
  | first %}

<p>

<strong>{{ item.year }}</strong><br>

{% if item.authors %}
{{ item.authors }}.
{% endif %}

{% if item.title %}
“{{ item.title }}.”
{% endif %}

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

{% if item.publication %}
<br>
<em>{{ item.publication }}</em>
{% endif %}

</p>

{% endfor %}



{% comment %}
==================================================
ACADEMIC STUDIES
==================================================
==================================================
This assumes type = academic-study in reception.csv
==================================================
{% endcomment %}

## Academic Studies

{% assign studies = site.data.reception
  | where: "type", "academic-study"
  | sort: "year"
  | reverse
%}

{% for item in studies %}

<p>

<strong>{{ item.year }}</strong><br>

{% if item.authors %}
{{ item.authors }}.
{% endif %}

{% if item.title %}
“{{ item.title }}.”
{% endif %}

{% if item.publication %}
<em>{{ item.publication }}</em>
{% endif %}

{% if item.publication_place %}
, {{ item.publication_place }}
{% endif %}

{% if item.publisher %}
: {{ item.publisher }}
{% endif %}

</p>

{% endfor %}



{% comment %}
==================================================
INTRODUCTIONS, FOREWORDS, PREFACES, PROLOGUES,
AND AFTERWORDS
==================================================
==================================================
Assumes type = introduction
==================================================
{% endcomment %}

## Introductions, Forewords, Prefaces, Prologues & Afterwords

{% assign introductions = site.data.reception
  | where: "type", "introduction"
  | sort: "year"
  | reverse
%}

{% for item in introductions %}

{% assign book = site.data.publications
  | where: "publication_id", item.publication_id
  | first %}

<p>

<strong>{{ item.year }}</strong><br>

{% if item.authors %}
{{ item.authors }}.
{% endif %}

{% if item.title %}
“{{ item.title }}.”
{% endif %}

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

</p>

{% endfor %}



{% comment %}
==================================================
INTERVIEWS
==================================================
==================================================
Assumes type = interview
==================================================
{% endcomment %}

## Interviews & Conversations

{% assign interviews = site.data.reception
  | where: "type", "interview"
  | sort: "year"
  | reverse
%}

{% for item in interviews %}

<p>

<strong>{{ item.year }}</strong><br>

{% if item.authors %}
{{ item.authors }}.
{% endif %}

{% if item.title %}
“{{ item.title }}.”
{% endif %}

{% if item.publication %}
<em>{{ item.publication }}</em>
{% endif %}

{% if item.publication_place %}
, {{ item.publication_place }}
{% endif %}

</p>

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
<a href="{{ item.local_copy | relative_url }}" target="_blank" rel="noopener">
Archived copy
</a>
{% endif %}

</p>

{% endif %}

{% endfor %}