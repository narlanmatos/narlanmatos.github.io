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

### [{{ book.title }}]({{ book.url }})

{% if book.cover %}
  <img src="{{ book.cover }}" alt="{{ book.title }} cover" style="max-width:200px;">
{% endif %}

**Year:** {{ book.year }}



---

{% endfor %}
