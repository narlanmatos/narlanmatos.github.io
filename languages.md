---

title: "Translations by Language"
permalink: /translations/languages/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image

  
    
---

*This page links to translations and bilingual editions by language. Entries include original books, anthologies, periodical publications, translations of individual poems, and festival publications or recordings.*

## Languages

| Language | Books | Anthologies | Periodicals | Poem Translations | Community | Festivals |
|:----------|------:|------------:|------------:|------------------:|----------:|----------:|

{% assign lt_languages = site.data.lyrics_translate_languages | sort: "language" %}

{% for row in lt_languages %}

{% assign language = row.language | strip %}

{% assign books = 0 %}
{% assign anthologies = 0 %}
{% assign periodicals = 0 %}
{% assign poems = 0 %}
{% assign community = 0 %}
{% assign festivals = 0 %}

{% for publication in site.data.publications %}

  {% assign found = false %}

  {% assign fields = "original_languages|translated_languages|publication_languages" | split: "|" %}

  {% for field in fields %}

    {% assign value = publication[field] %}

    {% if value %}

      {% assign values = value | split: ";" %}

      {% for item in values %}
        {% if item | strip == language %}
          {% assign found = true %}
        {% endif %}
      {% endfor %}

    {% endif %}

  {% endfor %}

  {% if found %}

    {% case publication.collection %}

      {% when "books" %}
        {% assign books = books | plus: 1 %}

      {% when "anthologies" %}
        {% assign anthologies = anthologies | plus: 1 %}

      {% when "periodicals" %}
        {% assign periodicals = periodicals | plus: 1 %}

      {% when "poems" %}
        {% assign poems = poems | plus: 1 %}

    {% endcase %}

  {% endif %}

{% endfor %}

{% if row.has_translation == "TRUE" %}
  {% assign community = 1 %}
{% endif %}

{% comment %}
Future:
{% for item in site.data.festival_languages %}
  {% if item.language == language %}
    {% assign festivals = festivals | plus: 1 %}
  {% endif %}
{% endfor %}
{% endcomment %}

{% assign slug = language | slugify %}

{% if row.has_page == "TRUE" %}
  {% assign page = site.languages | where: "slug", slug | first %}
{% else %}
  {% assign page = nil %}
{% endif %}

| {% if page %}[{{ language }}]({{ page.url | relative_url }}){% else %}{{ language }}{% endif %} | {{ books }} | {{ anthologies }} | {{ periodicals }} | {{ poems }} | {{ community }} | {{ festivals }} |

{% endfor %}

