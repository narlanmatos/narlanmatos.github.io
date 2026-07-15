---

title: "Collected Poems & Anthologies"
permalink: /translations/anthologies-translated/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image

feature_row:
  - image_path: /assets/images/translations/como-nacen.jpg
    title: "Cómo nacen las estrellas (2024)"
    url: /translations/como-nacen/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/translations/poetry-mens-lives.jpg
    title: "The Poetry of Men's Lives: an International Anthology (2004)"
    url: translations/poetry-mens-lives/
    btn_label: "View Book"
    btn_class: "btn--primary" 
      
  - image_path: /assets/images/translations/pesem.jpg
    title: "Pesem o Vetru in Mojem Zivljenju (2015)"
    url: /translations/pesem/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/translations/duet.jpg
    title: "Duet of Dots (Japanese Edition; 2015)"
    url: translations/duet/
    btn_label: "View Book"
    btn_class: "btn--primary"   
    
  - image_path: /assets/images/translations/duet-es.jpg
    title: "Dueto de puntos (Spanish Edition; 2020)"
    url: translations/duet-es/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/translations/duet-it.jpg
    title: "Duetto di Punti (Italian Edition; 2020)"
    url: translations/duet-it/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/translations/duet-fr.jpg
    title: "Duo de Points (French Edition; 2021)"
    url: translations/duet-fr/
    btn_label: "Voir le Livre"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/translations/provincia.jpg
    title: "La Provincia Oscura"
    url: translations/provincia/
    btn_label: "Visualizza il Libro"
    btn_class: "btn--primary"

    
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

*The following anthologies contain selected works of Narlan Matos, sometimes alongside those of other poets.*

{% assign books = site.data.publications
  | where: "type", "translated_anthology"
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
{% include feature_row id="feature_row_bilingual" %}