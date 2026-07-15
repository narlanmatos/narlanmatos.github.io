---

title: "Translations by Language"
permalink: /translations/languages/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image

  
feature_row_languages:
  - url: /translations/languages/english/
    btn_label: "English"
    btn_class: "btn--primary"
    
  - url: /translations/languages/french/
    btn_label: "French"
    btn_class: "btn--primary"
    
  - url: /translations/languages/german/
    btn_label: "German"
    btn_class: "btn--primary"
    
  - url: /translations/languages/japanese/
    btn_label: "Japanese"
    btn_class: "btn--primary"
    
  - url: /translations/languages/italian/
    btn_label: "Italian"
    btn_class: "btn--primary"
    
  - url: /translations/languages/lithuanian/
    btn_label: "Lithuanian"
    btn_class: "btn--primary"
    
  - url: /translations/languages/romanian/
    btn_label: "Romanian"
    btn_class: "btn--primary"
    
  - url: /translations/languages/russian/
    btn_label: "Russian"
    btn_class: "btn--primary"
    
  - url: /translations/languages/slovenian/
    btn_label: "Slovenian"
    btn_class: "btn--primary"
    
  - url: /translations/languages/spanish/
    btn_label: "Spanish"
    btn_class: "btn--primary"
---


Page under development. 


{% include feature_row id="feature_row_languages" %}

<!--*This page links to translations and bilingual editions by language. Entries include original books, anthologies, periodical publications, translations of individual poems, and festival publications or recordings.*-->


---

## <a href="https://lyricstranslate.com/en/narlan-matos-lyrics.html" target="_blank" rel="noopener">Community Translations on LyricsTranslate</a>

<table>
  <thead>
    <tr>
      <th>Language</th>
      <th style="text-align:right;">Poems</th>
    </tr>
  </thead>

  <!-- Portuguese -->
  <tbody>

  {% assign portuguese = site.data.lyrics_translate_languages
     | where: "language", "Portuguese" %}

  {% for row in portuguese %}

    <tr class="featured-language">

      <td>

        {% if row.slug %}

          <a href="{{ '/translations/languages/' | append: row.slug | append: '/' | relative_url }}">
            <strong>{{ row.language }}</strong>
          </a>

        {% else %}

          <strong>{{ row.language }}</strong>

        {% endif %}

      </td>

      <td style="text-align:right;">
        <strong>{{ row.n_poems }}</strong>
      </td>

    </tr>

  {% endfor %}

  </tbody>

  <tbody>
    <tr>
      <td colspan="2">
        <hr style="margin:.4em 0;">
      </td>
    </tr>
  </tbody>

  <!-- Other languages -->
  <tbody>

  {% assign languages = site.data.lyrics_translate_languages | sort: "language" %}

  {% for row in languages %}

    {% unless row.language == "Portuguese" %}

    <tr>

      <td>

        {% if row.slug %}

          <a href="{{ '/translations/languages/' | append: row.slug | append: '/' | relative_url }}">
            {{ row.language }}
          </a>

        {% else %}

          {{ row.language }}

        {% endif %}

      </td>

      <td style="text-align:right;">
        {{ row.n_poems }}
      </td>

    </tr>

    {% endunless %}

  {% endfor %}

  </tbody>

</table>

<!-- trying to make table. This does not work:


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

-->