---
type: bilingual_edition
title: "Antología Poética Bilingüe"
year: 2017
publisher: "Maoli Editorial"
isbn: "978-8494492433"
cover: "/assets/images/translations/antología.jpg"
buy_link: "https://www.amazon.com/gp/product/8494492438"

languages:
  - Portuguese
  - Spanish
  
translator:
  - "José Ángel García Caballero"

illustrator:
  - "Juan Carlos Mestre"
  
# Link back to original work (important for structure)
original_work: "xx"
---

*Antología poética bilingüe*... 

{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

<!--## Overview

This bilingual edition presents *{{ page.original_title }}* in its original language alongside its English translation. It allows readers to engage with the musicality of the original text while following the translated version.-->

---

## Languages

- Original language: {{ page.languages[0] }}
- Translation: {{ page.languages[1] }}

---

## Translator

{% for t in page.translator %}
- {{ t }}
{% endfor %}

---

## Illustrator

{% for t in page.illustrator %}
- {{ t }}
{% endfor %}

---

## Publication

- Publisher: {{ page.publisher }}
- Year: {{ page.year }}

---

## Related Work

This edition is based on:

  **{{ page.original_title }}**

<!--(Original-language collection in the Poetry section)-->

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




