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
# Critical Reception
# --------------------------------------------------------------------

reviews:
  - title: "La provincia oscura di Narlan Matos"
    author: "Silvia Leuzzi"
    publication: "La Tigre di Carta"
    url: "https://www.latigredicarta.it/2017/05/29/la-provincia-oscura-di-narlan-matos/"

  - title: "Dalla provincia oscura alla città del sole"
    author: "Marco Testi"
    publication: "Fili d'Aquilone"
    url: "https://www.filidaquilone.it/num045testi.html"

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

excerpt: []
---

{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

## Overview

{{ content }}

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
- **Translator{% if page.translators.size > 1 %}s{% endif %}:**
  {% for translator in page.translators %}
    {% unless forloop.first %}, {% endunless %}{{ translator }}
  {% endfor %}
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

{% if page.reviews.size > 0 %}
## Critical Reception

<ul>
{% for review in page.reviews %}
<li>
<strong>{{ review.title }}</strong><br>
{{ review.author }}
{% if review.publication %}
(<em>{{ review.publication }}</em>)
{% endif %}
{% if review.url %}
— <a href="{{ review.url }}" target="_blank" rel="noopener">Read review</a>
{% endif %}
</li>
{% endfor %}
</ul>

---
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
