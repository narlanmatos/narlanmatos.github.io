---
type: translated_anthology
title: "Cómo nacen las estrellas "

translators:
  - Lily Martínez Evangelista
  - Alisson Dias Bezerra
  - José Miguel Lemus
  - M. Emilia Barbosa
  - Maritza Salgueiro-Carlisle
  
year: 2024
publisher: "Valparaíso Ediciones"
isbn: "978-8410073845"

cover: "/assets/images/translations/como-nacen.jpg"
publisher_link: "https://valparaisoediciones.es/tienda/poesia/901-446-como-nacen-las-estrellas.html"
buy_link: "https://www.amazon.com/C%C3%B3mo-nacen-estrellas-Narlan-Matos/dp/8410073846"


# Languages
original_language:
  - Portuguese

translated_languages:
  - Spanish

  
# Link back to original work (important for structure)
original_work: "xx"
---

{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

## Overview

This Spanish-language collection brings together a selection of Narlan Matos's poetry,
beginning with his first book in 1997, [*Senhoras e Senhores: o Aamanhecer*]().

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

- Original language: {{ page.original_language }}
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

This edition contains poems originally published in  **{{ page.original_work }}**.


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




