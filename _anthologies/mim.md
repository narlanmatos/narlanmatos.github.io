---
type: chapbook
title: "Mim, Fim"
series: "Coleção Leve um Livro"
year: 2017
place: "Belo Horizonte, Brazil"
publisher: "Projecto Leve um Livro"
pages: 16
notes: "Micro-anthology distributed free as part of the Coleção Leve um Livro poetry project."

author:
  - Narlan Matos


language: Portuguese



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

*Mim, Fim* is a micro-anthology distributed free as part of the  *[Leve um Livro](https://anadigital.pro.br/2020/07/27/leve-um-livro/?utm_source=chatgpt.com)* poetry project.

---

## Publication

- Publisher: {{ page.publisher }}
- Year: {{ page.year }}

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




