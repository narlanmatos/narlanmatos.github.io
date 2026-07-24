---

title: "Selected Poems"
permalink: /poetry/selected-poems/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image
  
feature_row_poems:
  - image_path: /assets/images/feature/xx.jpg
    title: "Elegia ao Novo Mundo"
    excerpt: |
      Tu me perguntas meu amigo
      
      Onde eu estive durante meu longo silêncio...
    url: /poetry/poems/elegia-ao-novo-mundo/
    btn_label: "Read Full Poem"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/feature/xx.jpg
    title: "Pós-Colombianos"
    excerpt: |
      Por pouco
      
      Muito pouco...
    url: /poetry/poems/pos-colombianos/
    btn_label: "Read Full Poem"
    btn_class: "btn--primary"
    
  - image_path: /assets/images/feature/xx.jpg
    title: "Tzar"
    excerpt: |
      é colossal a espera por tudo
      
      pelo mar que o poente esconde e desenha…
    url: /poetry/poems/tzar/
    btn_label: "Read Full Poem"
    btn_class: "btn--primary"

---

*This page brings together the original Portuguese poems currently available to read on this website.*
*Each poem page includes publication information and links to other language versions.*

*As additional poems and translations are published on the website, this collection will continue to grow.*


## Featured Poems

{% include feature_row id="feature_row_poems" %}


## All Poems

{% assign originals = site.data.poems
  | where: "language", "Portuguese"
  | sort: "title" %}

{% for record in originals %}

  {% assign page = site.poems
    | where: "poem_id", record.poem_id
    | first %}

  {% if page %}

  <article class="archive__item">

    <h2>
      <a href="{{ page.url | relative_url }}">{{ record.title }}</a>
    </h2>

    {% if record.incipit %}
      <p>{{ record.incipit }}</p>
    {% endif %}

    <p>
      <a href="{{ page.url | relative_url }}">Read poem →</a>
    </p>

  </article>

  {% endif %}

{% endfor %}