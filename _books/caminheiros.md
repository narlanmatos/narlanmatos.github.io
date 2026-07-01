---
type: book
author: Narlan Matos
title: "Eu e Tu, Caminheiros Dessa Vida"
year: 2019
publisher: "Penalux"
isbn: "978-8558335676"
cover: "/assets/images/books/caminheiros.jpg"
publisher_link: "https://loja.editoralitteralux.com.br/eu-e-tu-caminheiros-dessa-vida"
read_link: "https://loja.editoralitteralux.com.br/image/catalog/PDF/9788558335676.pdf"
buy_link: "https://www.amazon.com.br/Eu-tu-caminheiros-dessa-vida/dp/8558335672/"

language: Portuguese

excerpt: "xxx"
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





