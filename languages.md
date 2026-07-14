---

title: "Translations by Language"
permalink: /translations/languages/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image

  
    
---

Page under development.

<!--*This page links to translations and bilingual editions by language. Entries include original books, anthologies, periodical publications, translations of individual poems, and festival publications or recordings.*-->

| Language | Books | Anthologies | Periodicals | Poems |
|:---------|------:|------------:|------------:|------:|
{% for row in site.data.lyrics_translate_languages %}

{% assign books = 0 %}
{% assign anthologies = 0 %}
{% assign periodicals = 0 %}
{% assign poems = 0 %}

{% assign language = row.language %}

{% if language == "Portuguese" %}

  {% for item in site.data.publications %}

    {% if item.collection == "books" %}
      {% assign books = books | plus: 1 %}
    {% endif %}

    {% if item.collection == "anthologies" %}
      {% assign anthologies = anthologies | plus: 1 %}
    {% endif %}

    {% if item.collection == "periodicals" %}

      {% assign found = false %}

      {% assign langs = item.original_languages | default: "" | split: ";" %}
      {% for lang in langs %}
        {% if lang | strip == "Portuguese" %}
          {% assign found = true %}
        {% endif %}
      {% endfor %}

      {% assign langs = item.translated_languages | default: "" | split: ";" %}
      {% for lang in langs %}
        {% if lang | strip == "Portuguese" %}
          {% assign found = true %}
        {% endif %}
      {% endfor %}

      {% if found %}
        {% assign periodicals = periodicals | plus: 1 %}
      {% endif %}

    {% endif %}

  {% endfor %}

{% else %}

  {% for item in site.data.publications %}

    {% assign translated = false %}

    {% assign langs = item.translated_languages | default: "" | split: ";" %}

    {% for lang in langs %}
      {% if lang | strip == language %}
        {% assign translated = true %}
      {% endif %}
    {% endfor %}

    {% if translated %}

      {% if item.collection == "translations" %}

        {% if item.type == "translated_book" %}
          {% assign books = books | plus: 1 %}
        {% else %}
          {% assign anthologies = anthologies | plus: 1 %}
        {% endif %}

      {% elsif item.collection == "periodicals" %}

        {% assign periodicals = periodicals | plus: 1 %}

      {% endif %}

    {% endif %}

  {% endfor %}

{% endif %}

{% for poem in site.data.poems %}
  {% if poem.language == language %}
    {% assign poems = poems | plus: 1 %}
  {% endif %}
{% endfor %}

| {{ language }} | {{ books }} | {{ anthologies }} | {{ periodicals }} | {{ poems }} |

{% endfor %}