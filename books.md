---
title: "Books"
permalink: /books/
layout: single
header:
  overlay_image: /assets/images/header.jpg  # header image
  caption: "Detail from artwork in Narlan Matos's *Antología poética bilingüe*, by legendary Spanish poet and artist Juan Carlos Mestre."

--------------

{% assign books = site.books | sort: "year" | reverse %}

{% for book in books %}

### [{{ book.title }}]({{ book.url }})

**Year:** {{ book.year }}

{{ book.excerpt }}

---

{% endfor %}
