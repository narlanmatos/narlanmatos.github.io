---
type: translated_anthology
title: "Duet of Dots"
year: 2015
publisher: "Nihon Kokusai Shijin Kyokai"
cover: "/assets/images/translations/duet.jpg"
buy_link: "https://www.amazon.com/Duet-Dots-Japanese-Maki-Starfield-ebook/dp/B018PH0YCS/"

authors:
  - Narlan Matos
  - Maki Starfield

original_languages: 
  - Portuguese
  - Japanese
  
language: 
  - Japanese

translator: 
  - "Maki Starfield"
  
editor: 
  - "Mariko Sumikura"

illustrator:
  - "James Spitzer "
  
# Link back to original work (important for structure)
original_work: "xx"

excerpt: "xxx"
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

<!--
---

## Related Work

This edition is based on:

  **{{ page.original_title }}**

(Original-language collection in the Poetry section)-->

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




