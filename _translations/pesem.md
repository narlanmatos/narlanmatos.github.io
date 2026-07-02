---
type: translated_anthology
title: "Pesem o Vetru in Mojem Zivljenju"

translators:
  - "Mojca Medvedšek"
  - "Blažka Müller Pograjc"

  
year: 2015
publisher: "Center za slovensko književnost"
isbn: ""

cover: "/assets/images/translations/pesem.jpg"



# Languages
original_language: Portuguese

translated_language: Slovenian


  
# Link back to original work (important for structure)
original_work: "xx"

excerpt: "xxx"
---

{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

## Overview

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
- Translation: {{ page.translated_language }}

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
