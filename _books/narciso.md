---
type: book
author: Narlan Matos
title: "Narciso selvagem"
year: 2022
publisher: "Penalux"
cover: "/assets/images/books/narciso.jpg"
publisher_link: "https://loja.editoralitteralux.com.br/narciso-selvagem"
read_link: "https://loja.editoralitteralux.com.br/image/catalog/PDF/9786558623397.pdf"

language: Portuguese

# Link to translations (important bridge)
has_translations: true
translation_group: "narciso-selvagem"
translation_languages:
  - Italian
  - English
  - French
---


{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

## Overview

*{{ page.title }}* is a poetry collection first published in {{ page.year }} by {{ page.publisher }}.
Written in {{ page.language }}, it forms part of Narlan Matos’s core poetic corpus.

<!--The work explores themes of memory, language, landscape, and transformation.-->

{% if page.read_link %}
<p>
  <a href="{{ page.read_link }}"
     class="btn btn--primary"
     target="_blank"
     rel="noopener">
     Read Sample
  </a>
</p>
{% endif %}
---

## Publication

- Year: {{ page.year }}
- Publisher: {{ page.publisher }}
- Language: {{ page.language }}
{% if page.isbn %}
- ISBN: {{ page.isbn }}
{% endif %}


{% if page.publisher_link %}
<p>
  <a href="{{ page.publisher_link }}"
     class="btn btn--primary"
     target="_blank"
     rel="noopener">
     View on Publisher's Site
  </a>
</p>
{% endif %}

--- 

## International Reception

{% if page.translation_languages %}
<p>Poems from <em>{{ page.title }}</em> have appeared in translation in {% assign langs = page.translation_languages %}{% if langs.size == 1 %}{{ langs[0] }}{% elsif langs.size == 2 %}{{ langs[0] }} and {{ langs[1] }}{% else %}{% for lang in langs %}{% if forloop.last %}and {{ lang }}{% else %}{{ lang }}{% unless forloop.index == langs.size | minus: 1 %}, {% endunless %}{% endif %}{% endfor %}{% endif %}.</p>
{% endif %}

#### Italian Translation
[Selected Poems translated by Manuela Colombo, published by *Fili d’Aquilone*](https://www.filidaquilone.it/num063colombo.html)

## Reviews

- Colombo, Manuela. “Narlan Matos, Narciso selvagem.” *Fili d’Aquilone*, no. 63 (2023). Italian introduction and translations from *Narciso selvagem*. [Read article](https://www.filidaquilone.it/num063colombo.html).





{% if page.buy_link %}
<p>
  <a href="{{ page.buy_link }}"
     class="btn btn--primary"
     target="_blank"
     rel="noopener">
     Buy this Book
  </a>
</p>
{% endif %}