---
type: bilingual_edition
title: "Eu Cânt Pentru Oameni de Bine"

translators:
  - Ana Vrǎjitoru
  
year: 2023
publisher: "EIKON"
isbn: "9786064909404"

cover: "/assets/images/translations/canto-ro.jpg"
publisher_link: "https://www.librariaeikon.ro/poezie/1584-eu-cant-pentru-oameni-de-bine-canto-aos-homens-de-boa-vontade.html"

# Languages
original_languages:
  - Portuguese

translated_languages:
  - Romanian

# Link back to original work (important for structure)
original_work: "Canto aos Homens de Boa Vontade"

excerpt: "xxx"
---

{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

## Overview

This is a Russian-language translation of Narlan Matos's 2018 book [*Canto aos Homens de Boa Vontade*](/poetry/books/canto).

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

This edition is a translation of [*Canto aos Homens de Boa Vontade*](/poetry/books/canto).


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


