---

title: "Books"
permalink: /poetry/books/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image


    
---

# Original Books

The following original poetry books by Narlan Matos, published in Portuguese between 1997 and the present, form Narlan Matos’s core poetic corpus.
Together these volumes trace the evolution of a body of work exploring memory, language, identity, migration, spirituality, and the human condition. 
Many have subsequently appeared in translation or inspired multilingual editions, which are linked from the individual book pages.

{% assign books = site.data.publications
  | where: "collection", "books"
  | sort: "publication_date" %}
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