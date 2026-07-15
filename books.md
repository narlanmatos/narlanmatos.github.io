---

title: "Books"
permalink: /poetry/books/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image

feature_row:
  - image_path: /assets/images/books/rebanhos.jpg
    title: "Rebanhos de Estrelas (2023)"
    excerpt: ""
    url: poetry/books/rebanhos/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/books/narciso.jpg
    title: "Narciso selvagem (2022)"
    excerpt: ""
    url: poetry/books/narciso/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/books/caminheiros.jpg
    title: "Eu e Tu, Caminheiros Dessa Vida (2019)"
    excerpt: ""
    url: poetry/books/caminheiros/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/books/canto.jpg
    title: "Canto aos Homens de Boa Vontade (2018)"
    excerpt: ""
    url: poetry/books/canto/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/books/alaude.jpg
    title: "Um Alaúde, a Península e Teus Olhos Negros (2017)"
    excerpt: ""
    url: poetry/books/alaude/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/books/elegia.jpg
    title: "Elegia ao Novo Mundo e outros poemas (2012)"
    excerpt: ""
    url: poetry/books/elegia/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/books/acampamento.jpg
    title: "No Acampamento das Sombras (2001)"
    excerpt: ""
    url: poetry/books/acampamento/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/books/senhoras.jpg
    title: "Senhoras e senhores: o amanhecer (1997)"
    excerpt: ""
    url: poetry/books/senhoras/
    btn_label: "View Book"
    btn_class: "btn--primary"
    
---

# Original Books

The following original poetry books by Narlan Matos, published in Portuguese between 1997 and the present, form Narlan Matos’s core poetic corpus.
Together these volumes trace the evolution of a body of work exploring memory, language, identity, migration, spirituality, and the human condition. 
Many have subsequently appeared in translation or inspired multilingual editions, which are linked from the individual book pages.*

{% assign books = site.data.publications
  | where: "collection", "books"
  | sort: "publication_date" %}

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