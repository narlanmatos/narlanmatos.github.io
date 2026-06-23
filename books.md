---

title: "Books"
permalink: /poetry/books
layout: single
header:
  overlay_image: /assets/images/header.jpg  # header image
  caption: "Detail from artwork in Narlan Matos' *Antología poética bilingüe*, by legendary Spanish poet and artist Juan Carlos Mestre."

---

# Books

{% assign books = site.books | sort: "year" | reverse %}

{% for book in books %}

{% capture feature_row %}
- image_path: {{ book.cover }}
  alt: "{{ book.title }}"
  title: "{{ book.title }}"
  excerpt: >
    {{ book.author }}
    {% if book.translator %}
    <br><em>Translated by {{ book.translator }}</em>
    {% endif %}
    <br><br>
    {{ book.excerpt }}
  url: {{ book.url }}
  btn_label: "View Book"
  btn_class: "btn--primary"
{% endcapture %}

{% assign feature_row = feature_row | yaml_to_object %}

{% include feature_row id=feature_row type="left" %}

---

{% endfor %}
