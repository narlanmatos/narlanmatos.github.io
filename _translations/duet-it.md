---
type: translated_anthology
title: "Duet of Dots (Spanish Edition)"
year: 2020
publisher: "JUNPA Books"
ISBN: " 978-1071551486"
cover: "/assets/images/translations/duet-it.jpg"
buy_link: "https://www.amazon.com/Duetto-Punti-Italian-Maki-Starfield-ebook/dp/B08BZ4ZJCZ/ref=sr_1_6"
read_link: "https://www.amazon.com/Duetto-Punti-Italian-Maki-Starfield-ebook/dp/B08BZ4ZJCZ/ref=sr_1_6"

authors:
  - Narlan Matos
  - Maki Starfield

original_languages: 
  - Portuguese
  - Japanese

language: Italian
  
editions:
  - Japanese
  - Portuguese
  - Spanish
  - Italian

translator: 
  
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
- [Portuguese](/poetry/anthologies/duet-pt)
- [Spanish](/translations/duet-es)
- Italian  (this edition)

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




