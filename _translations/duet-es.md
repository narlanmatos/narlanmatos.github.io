---
type: translated_anthology
title: "Dueto de Puntos (Spanish Edition)"
year: 2020
publisher: "JUNPA Books"
ISBN: " 978-1071565483"
cover: "/assets/images/translations/duet-es.jpg"
buy_link: "https://www.amazon.com/Dueto-puntos-Occidente-Oriente-Solidaridad-Dialogo-ebook/dp/B08K9G45B9/ref=sr_1_5"
read_link: "https://www.amazon.com/Dueto-puntos-Occidente-Oriente-Solidaridad-Dialogo-ebook/dp/B08K9G45B9/ref=sr_1_5"

authors:
  - Narlan Matos
  - Maki Starfield

original_languages: 
  - Portuguese
  - Japanese

language: Spanish
  
editions:
  - Japanese
  - Portuguese
  - Spanish
  - Italian

translator: 
  - "Hadit Montero"
  
editor: 
  - "Mariko Sumikura"

illustrator:
  - "James Spitzer "
  
# Link back to original work 
original_work: "/translations/duet/"

excerpt: "*Duet of Dots* is a collaboration by Narlan Matos and the Japanese poetess Maki Starfield, with translations published in multiple languages."
---

{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

<!--## Overview
-->


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

- Original languages: Portuguese, Japanese 
- Translation: {{ page.language }}

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

## Editions
- [Japanese](/translations/duet/) (original edition)
- [Portuguese](/anthologies/duet-pt)
- Spanish (this edition)
- [Italian](/translations/duet-it)

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




