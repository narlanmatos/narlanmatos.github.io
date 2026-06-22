---
type: book
author: Narlan Matos
title: "Um Alaúde, a Península e Teus Olhos Negros"
year: 2017
publisher: "Penalux"
isbn: "8558332274"
cover: "/assets/images/books/alaude.jpg"
publisher_link: "https://loja.editoralitteralux.com.br/um-alaude-a-peninsula-e-teus-olhos-negros"
read_link: "https://loja.editoralitteralux.com.br/image/catalog/PDF/9788558332279.pdf"
buy_link: "https://www.amazon.com.br/Ala%C3%BAde-Pen%C3%ADnsula-Teus-Olhos-Negros/dp/8558332274/"

language: Portuguese
---


{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

## Overview

*{{ page.title }}* is a poetry collection first published in {{ page.year }} by {{ page.publisher }}.
Written in {{ page.language }}, it forms part of Narlan Matos’s core poetic corpus.

<!--The work explores themes of memory, language, landscape, and transformation.-->

---

## Publication

- Year: {{ page.year }}
- Publisher: {{ page.publisher }}
- Language: {{ page.language }}
{% if page.isbn %}
- ISBN: {{ page.isbn }}
{% endif %}


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





