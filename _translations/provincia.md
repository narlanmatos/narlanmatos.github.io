---
title: "La Provincia Oscura"
permalink: /translations/provincia/
cover: "/assets/images/translations/provincia.jpg"

# classification
collection: translations
type: translated_anthology

# languages & translation
original_language: Portuguese
translated_language: Italian

translators:
  - "Giorgio Mobili"

# publication info  
year: 2016
publisher: "Fili d'Aquilone"
publication_place: "Rome, Italy"
isbn: "978-88-97490-17-3"

# link to original work
original_work:

# awards
awards: []

# critical reception
reviews:
  - title: "La provincia oscura di Narlan Matos"
    author: "Silvia Leuzzi"
    publication: "La Tigre di Carta"
    url: https://www.latigredicarta.it/2017/05/29/la-provincia-oscura-di-narlan-matos/
    
  - title: "Dalla provincia oscura alla città del sole"
    author: "Marco Testi"
    publication: "Fili d'Aquilone"
    url: https://www.filidaquilone.it/num045testi.html

# read and buy links
read_link: "https://www.efilidaquilone.it/fili_16_la_provincia_oscura_anteprima.pdf"
publisher_link: "https://www.efilidaquilone.it/Scheda_Fili_16.pdf"
buy_link: "https://www.ibs.it/provincia-oscura-testo-portoghese-a-libro-narlan-matos/e/9788897490173"


# performances
videos:

gallery:
  - "/assets/images/translations/provincia.jpg"


# excerpt:
excerpt: []
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

## Translator

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
