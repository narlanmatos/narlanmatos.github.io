---
title: "La Provincia Oscura"
permalink: /translations/provincia/
cover: "/assets/images/translations/provincia.jpg"

# --------------------------------------------------------------------
# Classification
# --------------------------------------------------------------------

collection: translations
type: translated_anthology

# --------------------------------------------------------------------
# Languages
# --------------------------------------------------------------------

original_language: Portuguese
translated_language: Italian

translators:
  - Giorgio Mobili

# --------------------------------------------------------------------
# Publication
# --------------------------------------------------------------------

year: 2016
publisher: "Edizioni Fili d'Aquilone"
publication_place: "Rome, Italy"
series: "I Fili"
pages: 138
isbn: "978-88-97490-17-3"

# --------------------------------------------------------------------
# Relationship to Original Works
# --------------------------------------------------------------------

original_works: []

# Example:
# original_works:
#   - title: Rebanhos de Estrelas
#     url: /poetry/books/rebanhos/
#
#   - title: Narciso Selvagem
#     url: /poetry/books/narciso/

# --------------------------------------------------------------------
# Awards
# --------------------------------------------------------------------

awards: []

# Example:
# awards:
#   - title: Poetry Book of the Year
#     organization: Romanian Writers Association
#     year: 2023

# --------------------------------------------------------------------
# External Resources
# --------------------------------------------------------------------

read_link: "https://www.efilidaquilone.it/fili_16_la_provincia_oscura_anteprima.pdf"
publisher_link: "https://www.efilidaquilone.it/Scheda_Fili_16.pdf"
buy_link: "https://www.ibs.it/provincia-oscura-testo-portoghese-a-libro-narlan-matos/e/9788897490173"

# --------------------------------------------------------------------
# Media
# --------------------------------------------------------------------

videos: []

gallery:
  - "/assets/images/translations/provincia.jpg"


# --------------------------------------------------------------------
# Descriptive Text 
# --------------------------------------------------------------------
excerpt: []

overview_description: |
  *La Provincia Oscura* is an Italian-Portuguese bilingual edition of selected
  poems by Narlan Matos, translated by Giorgio Mobili and published by Fili
  d'Aquilone in 2016. 
  
  The volume introduces Italian readers to Narlan Matos's
  poetry through parallel Portuguese and Italian texts.
---

{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

{% if page.overview_description %}
## Overview

{{ page.overview_description | markdownify }}

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

---

## Bibliographic Information

- **Original language:** {{ page.original_language }}

- **Translation:** {{ page.translated_language }}

{% if page.translators %}
- **Translator{% if page.translators.size > 1 %}s{% endif %}:** {{ page.translators | join: ", " }}
{% endif %}

- **Publisher:** {{ page.publisher }}

{% if page.publication_place %}
- **Place:** {{ page.publication_place }}
{% endif %}

{% if page.series %}
- **Series:** {{ page.series }}
{% endif %}

- **Year:** {{ page.year }}

{% if page.pages %}
- **Pages:** {{ page.pages }}
{% endif %}

{% if page.isbn %}
- **ISBN:** {{ page.isbn }}
{% endif %}

---

{% if page.original_works.size > 0 %}
## Original Work{% if page.original_works.size > 1 %}s{% endif %}

This edition contains poems originally published in:

<ul>
{% for work in page.original_works %}
<li>
{% if work.url %}
<a href="{{ work.url }}">{{ work.title }}</a>
{% else %}
{{ work.title }}
{% endif %}
</li>
{% endfor %}
</ul>

---
{% endif %}

{% if page.awards.size > 0 %}
## Awards

<ul>
{% for award in page.awards %}
<li>
<strong>{{ award.title }}</strong>
{% if award.organization %}
— {{ award.organization }}
{% endif %}
{% if award.year %}
({{ award.year }})
{% endif %}
</li>
{% endfor %}
</ul>

---
{% endif %}

{% assign reception_items = site.data.reception | where: "related_work_url", page.url %}

{% if reception_items.size > 0 %}
## Critical Reception

<ul>
{% for item in reception_items %}
<li>
<strong>{{ item.title }}</strong><br>

{% if item.authors %}
{{ item.authors }}
{% endif %}

{% if item.publication %}
(<em>{{ item.publication }}</em>{% if item.year %}, {{ item.year }}{% endif %})
{% elsif item.year %}
({{ item.year }})
{% endif %}

{% if item.type %}
— 
{% if item.type == "academic" %}
[Academic study]
{% elsif item.type == "essay" %}
[Critical essay]
{% elsif item.type == "review" %}
[Review]
{% else %}
[{{ item.type | capitalize }}]
{% endif %}
{% endif %}

{% if item.url %}
— <a href="{{ item.url }}" target="_blank" rel="noopener">Read</a>
{% endif %}

</li>
{% endfor %}
</ul>
{% endif %}

## External Resources

{% if page.publisher_link %}
<p>
<a href="{{ page.publisher_link }}"
   class="btn btn--primary"
   target="_blank"
   rel="noopener">
Publisher
</a>
</p>
{% endif %}

{% if page.buy_link %}
<p>
<a href="{{ page.buy_link }}"
   class="btn btn--primary"
   target="_blank"
   rel="noopener">
Purchase
</a>
</p>
{% endif %}


