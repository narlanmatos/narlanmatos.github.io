---

title: "Collected Poems & Anthologies"
permalink: /poetry/anthologies/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image

feature_row:
  - image_path: /assets/images/books/duet-pt.jpg
    title: "Dueto de Pontos (Portuguese Edition)"
    url: /poetry/anthologies/duet-pt/
    excerpt: "Collaboration between Narlan Matos and the Japanese poetess Maki Starfield, with translations published in multiple languages."
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/books/mim.jpg
    title: "Mim, Fim"
    excerpt: "Micro-anthology distributed free as part of the *Leve um Livro* poetry project."
    url: /poetry/anthologies/mim/
    btn_label: "View Micro-anthology"
    btn_class: "btn--primary"

feature_row_bilingual:
  - image_path: /assets/images/translations/antologia.jpg
    title: "Antología Poética Bilingüe"
    url: /translations/antologia/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/translations/autores.jpg
    title: "Autores Baianos"
    url: /translations/autores/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/translations/poetinis.jpg
    title: "Poetinis Druskinink ruduo 2012 (Drukininkai Poetic fall 2012)"
    url: /translations/poetinis/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
---
## Anthologies in Portuguese

*The following anthologies include selected poems in Portuguese originally published in one or more [books](/poetry/books/).*

{% assign books = site.data.publications
  | where: "collection", "anthologies"
  | sort: "publication_date"
  | reverse %}

<div class="feature__wrapper">

{% for book in books %}

<div class="feature__item" style="margin-bottom:2.5em;">

  <div class="archive__item">

    {% if book.cover %}
    <div class="archive__item-teaser">
      <a href="{{ book.url | relative_url }}">
        <img src="{{ book.cover | relative_url }}"
             alt="{{ book.title }} cover">
      </a>
    </div>
    {% endif %}

    <div class="archive__item-body">

      <h3 class="archive__item-title">
        <a href="{{ book.url | relative_url }}">
          {{ book.title }}
        </a>
      </h3>

      {% if book.subtitle %}
      <p><em>{{ book.subtitle }}</em></p>
      {% endif %}

      <p>

      {% if book.publication_date %}
      {{ book.publication_date }}
      {% endif %}

      {% if book.publisher %}
      · {{ book.publisher }}
      {% endif %}

      </p>

      <p>

      <a class="btn btn--primary"
         href="{{ book.url | relative_url }}">
         View book
      </a>

      </p>

    </div>

  </div>

</div>

{% endfor %}

</div>

## Bilingual and Multilingual Anthologies

*The following anthologies include originals in Portuguese alongside translations in one or more additional languages (see also [Translated Anthologies](/translations/anthologies-translated/)).*

{% include feature_row id="feature_row_bilingual" %}