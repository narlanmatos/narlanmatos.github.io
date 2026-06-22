---
type: book
title: "Eu e Tu, Caminheiros Dessa Vida"
author: Narlan Matos
year: 2019
publisher: "Penalux"
isbn: "8558335672"
cover: "/assets/images/books/caminheiros.jpg"
publisher_link: "https://loja.editoralitteralux.com.br/eu-e-tu-caminheiros-dessa-vida"
read_link: "https://loja.editoralitteralux.com.br/image/catalog/PDF/9788558335676.pdf"
buy_link: "https://www.amazon.com.br/Eu-tu-caminheiros-dessa-vida/dp/8558335672/"

languages:
  - Portuguese
---


{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

## Overview

*{{ page.title }}* is a poetry collection first published in {{ page.year }} by {{ page.publisher }}. Written in {{ page.language }}, it forms part of the author’s core poetic corpus.

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

## Editions

### Portuguese Edition
Published 2019 by Penalux.



