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
    


---

*This page brings together the poems currently available to read on this website. *
*Written originally in Portuguese, these works are presented alongside translations into multiple languages where available. *
*Each poem page includes publication information and links to other language versions.*

*As additional poems and translations are published on the website, this collection will continue to grow.*


## Featured Poems

{% include feature_row id="feature_row_poems" %}


---

{% assign originals = site.poems
  | where: "language", "Portuguese"
  | sort: "publication_date"
  | reverse %}

{% if originals.size > 0 %}

<div class="entries-list">

{% for poem in originals %}

<article class="archive__item">

<h2 class="archive__item-title">