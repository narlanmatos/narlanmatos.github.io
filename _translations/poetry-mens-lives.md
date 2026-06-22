---
type: translated_anthology
title: "The Poetry of Men's Lives: an International Anthology"

# Editorial info (important for anthologies)
editor:
  - "Fred Moramarco"
  - "Al Zolynas"

translators:
  - "Narlan Matos"
  - "Al Zolynas"
  - "many more translators"
  
year: 2004
publisher: "University of Georgia Press"
isbn: "978-0820326498"

cover: "/assets/images/translations/poetry-mens-lives.jpg"
read_link: "https://books.google.co.th/books/about/The_Poetry_of_Men_s_Lives.html"
buy_link: "https://www.amazon.com/Poetry-Mens-Lives-International-Anthology/dp/0820326496"


# Languages
original_languages:
  - Portuguese
  - many more languages

translated_languages:
  - English


# Scope metadata
countries_represented:
  - Brazil
  - many more countries
  
# Link back to original work (important for structure)
original_work: "xx"
---

{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

## Overview

This English-language anthology, edited by Fred Moramarco and Al Zolynas, brings together more than 250 contemporary poets from almost 100 countries, including Narlan Matos of Brazil.

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

- Original language: Portuguese, many more
- Translation: English

---

## Translators

Translators include Narlan Matos and Al Zolynas (translators of Narlan Matos's poem "My Fathers House") and many more.

---

## Publication

- Publisher: {{ page.publisher }}
- Year: {{ page.year }}


---

## Related Work

This edition contains Narlan Matos's poem "My Father's House" from **{{ page.original_work }}**.


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




