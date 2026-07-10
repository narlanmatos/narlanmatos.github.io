---
type: translated_book
title: "я И Ты -ПУТНИКИ В ЭТОЙ ЖИЗНИ"

translators:
  - Irina Feshchenko-Skvortsova
  
year: 2023
publisher: ""
isbn: "978-5604732496"

cover: "/assets/images/books/caminheiros-ru.jpg"

# Languages
original_languages:
  - Portuguese

translated_languages:
  - Russian

# Link back to original work (important for structure)
original_work: "/poetry/books/caminheiros/"

excerpt: "xxx"
---

{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

## Overview

This is a Russian-language translation of Narlan Matos's 2019 book [*Eu e Tu, Caminheiros Dessa Vida*](/poetry/books/caminheiros).

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

## Languages

- Original language: {{ page.original_languages }}
- Translation: {{ page.translated_languages }}

---

## Translators

{% for translator in page.translators %}
- {{ translator }}
{% endfor %}

---

## Publication

- Publisher: {{ page.publisher }}
- Year: {{ page.year }}


---

## Related Work

This edition is a translation of [*Eu e Tu, Caminheiros Dessa Vida*](/poetry/books/caminheiros).


---


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


