---

title: "Eu Cânt Pentru Oameni de Bine"
permalink: /translations/canto-ro/
cover: "/assets/images/translations/canto-ro.jpg"

# --------------------------------------------------------------------
# Classification
# --------------------------------------------------------------------

collection: translations
type: bilingual_edition

# --------------------------------------------------------------------
# Languages
# --------------------------------------------------------------------

original_language: Portuguese
translated_language: Romanian

translators:
  - Ana Vrǎjitoru

# --------------------------------------------------------------------
# Publication
# --------------------------------------------------------------------

year: 2023
publisher: "EIKON"
publication_place: []
series: []
pages: []
isbn: "9786064909404"
  
  

# --------------------------------------------------------------------
# Relationship to Original Works
# --------------------------------------------------------------------

original_works:   
  - title: "Canto aos Homens de Boa Vontade" 
    url: /poetry/books/canto/

# --------------------------------------------------------------------
# External Resources
# --------------------------------------------------------------------

read_link: []
publisher_link: "https://www.librariaeikon.ro/poezie/1584-eu-cant-pentru-oameni-de-bine-canto-aos-homens-de-boa-vontade.html"
buy_link: []

# --------------------------------------------------------------------
# Media
# --------------------------------------------------------------------

videos: []

gallery:
  - "/assets/images/translations/provincia.jpg"


# --------------------------------------------------------------------
# Descriptive Text 
# --------------------------------------------------------------------

overview_description: |
   This bilingual edition contains Portuguese originals and Romanian-language
   translation of Narlan Matos's 2018 book *Canto aos Homens de Boa Vontade*.
   
   It was recipient of the 2024 Premiul pentru Traducere (Translation Prize).


---

{% if page.cover %}
<figure class="align-center">
  <img src="{{ page.cover | relative_url }}" alt="{{ page.title }} cover">
</figure>
{% endif %}

## Overview

This bilingual edition contains Portuguese originals and Romanian-language translation of Narlan Matos's 2018 book [*Canto aos Homens de Boa Vontade*](/poetry/books/canto/).

It was recipient of the 2024 Premiul pentru Traducere (Translation Prize).

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

- Original language: {{ page.original_languages }}
- Translation: {{ page.translated_languages }}

---

## Translators

{% for translator in page.translators %}
- {{ translator }}
{% endfor %}

---

## Publication

- Publisher: {{ page.publisher }}
- Year: {{ page.year }}


---

## Related Work

- [*Canto aos Homens de Boa Vontade*](/poetry/books/canto)


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


