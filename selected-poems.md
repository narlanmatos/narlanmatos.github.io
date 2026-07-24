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

{% assign originals = site.poems
  | where: "language", "Portuguese"}

{% if originals.size > 0 %}

<div class="entries-list">

{% for poem in originals %}

<article class="archive__item">

<h2 class="archive__item-title">
<a href="{{ poem.url | relative_url }}">{{ poem.title }}</a>
</h2>

{% if poem.original_title and poem.original_title != poem.title %}
<p><em>{{ poem.original_title }}</em></p>
{% endif %}

{% if poem.first_publication %}
<p>
<strong>First published:</strong> {{ poem.first_publication }}
</p>
{% endif %}

{% if poem.excerpt %}
<p>{{ poem.excerpt }}</p>
{% endif %}

<p>
<a href="{{ poem.url | relative_url }}">Read poem →</a>
</p>

</article>

{% endfor %}

</div>

{% endif %}