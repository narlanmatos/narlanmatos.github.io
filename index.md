---
title: "Narlan Matos"
layout: splash
permalink: /
header:
  overlay_image: /assets/images/header.jpg  # header image
  caption: "Detail from artwork in Narlan Matos's *Antología poética bilingüe*, by legendary Spanish poet and artist Juan Carlos Mestre."
  actions:
    - label: "About"
      url: "/about/"

feature_row_hero: 
  - image_path: /assets/images/portraits/Narlan-casa.jpg
  - title: "Narlan Matos"
    excerpt: "Brazilian-American poet, scholar, and musician."
    url: /poetry/
    btn_label: "Explore Poetry"
    btn_class: "btn--primary"

feature_row_book:
  - image_path: /assets/images/books/narciso.jpg
    title: "Narciso selvagem"
    excerpt: ""
    url: poetry/books/narciso/
    btn_label: "View Book"
    btn_class: "btn--primary"

    
feature_row_recording:
  - image_path: /assets/images/audio/sarau.jpg
    title: "Sarao no Pátio das Flores"
    excerpt: "A recitation of Narlan's poetry by Luiz Caldas."
    url: https://www.luizcaldas.com.br/
    btn_label: "Listen on Luiz Caldas's Website"
    btn_class: "btn--primary"
    
feature_row_explore:
  - image_path: /assets/images/features/books.jpg
    title: "Poetry"
    excerpt: "Original poetry collections, selected poems, and the evolving body of work."
    url: /poetry/
    btn_label: "Explore Poetry"
    btn_class: "btn--primary"
  - image_path: /assets/images/features/translations.jpg
    title: "Translations"
    excerpt: "Poetry published across multiple languages, countries, and cultural contexts."
    url: "/translations/"
    btn_label: "View translations"
    btn_class: "btn--primary"
  - image_path: /assets/images/features/reception.jpg
    title: "Critical Reception"
    excerpt: "Essays, reviews, interviews, and critical responses to the work."
    url: "/reception/"
    btn_label: "Read Criticism"
    btn_class: "btn--primary"
---

<!-- 1. Hero section - 
Professional portrait, name, one-sentence description (e.g., "Brazilian-American poet, translator, scholar, and musician."), 
optional call-to-action: Explore the Poetry or Latest Book-->

{% include feature_row id="feature_row_hero" %}

## Featured Book
<!--Highlight the most recent or most significant poetry collection with cover, brief description, and link.-->
{% include feature_row id="feature_row_book" %}

## Introduction
<!--A concise biography (75–150 words), with a link to the full Biography page.-->

## Featured Poems
<!--One to three representative poems or excerpts with links to read more.-->

## International Reach
<!--A brief section noting translations, major awards, or publications in multiple languages, linking to the Translations page.-->

## Latest News
<!--The two or three most recent events, publications, or readings.-->

## Explore the Archive

<!--Visual cards linking to the site's major sections:
Poetry
Translations
Critical Reception
Scholarship
Music-->

{% include feature_row id="feature_row_explore" %}


