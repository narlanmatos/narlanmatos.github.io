---

title: "Poems in English"
language: English
slug: english-selected-poems




    
---

*This page brings together the original Portuguese poems currently available to read on this website.*
*Each poem page includes publication information and links to other language versions.*

*As additional poems and translations are published on the website, this collection will continue to grow.*

## All English Poems

{% assign originals = site.data.poems
  | where: "language", "English"
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
---

*For English books, selected poems, and performances, return to [English Translations](/translations/languages/english/).*

