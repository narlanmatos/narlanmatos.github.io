---
type: book
author: Narlan Matos
title: "Senhoras e senhores: o amanhecer"
year: 1997
publisher: "Fundação Casa de Jorge Amado"
cover: "/assets/images/books/senhoras.jpg"


language: Portuguese

excerpt: "Winner of Prêmio Braskem da Fundação Casa de Jorge Amado (1997)"
---


{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

## Overview

*{{ page.title }}* was Narlan Matos's first poetry collection, published in {{ page.year }} by {{ page.publisher }}.
Written in {{ page.language }}, it forms part of Narlan Matos’s core poetic corpus.

In 1997, it won the Prêmio Braskem da [Fundação Casa de Jorge Amado](https://www.jorgeamado.org.br/?lang=en) (Braskem Prize of the Casa de Jorge Amado Foundation).




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





