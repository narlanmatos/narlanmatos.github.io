---

title: "Translated Books"
permalink: /translations/books-translated/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image



---

*The following are translations of Narlan Matos's [original books](/poetry/books/).*

{% assign books = site.data.publications
  | where: "type", "translated_book"
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