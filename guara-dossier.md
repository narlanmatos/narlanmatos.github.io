---
title: "Guará Dossier: Narlan Matos"
permalink: /reception/criticism/academic/gaura-dossier/
layout: single

collection: guara-dossier

publication: "Guará - Revista de Linguagem e Literatura"
volume: "15"
issue: "1"
year: 2025

url: "https://seer.pucgoias.edu.br/index.php/guara/issue/view/488"

image: "/assets/images/criticism/guara-cover.jpg"

sidebar:
  - image: /assets/images/criticism/guara-cover.jpg
---

{% assign articles = site.data.reception | where: "collection", page.collection %}

{% for item in articles %}

### {{ item.title }}

**{{ item.authors }}**  
*{{ item.publication }}* ({{ item.year }})

{% if item.doi %}
DOI: https://doi.org/{{ item.doi }}
{% endif %}

{% if item.url %}
<a href="{{ item.url }}">Read article</a>
{% endif %}

{% endfor %}