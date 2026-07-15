---

title: "Translations by Language"
permalink: /translations/languages/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image

  

---

The table below summarizes the languages into which Narlan Matos's work has been translated or published.
It includes books, anthologies, poetry published in literary journals and other periodicals, individual poems available on this website, and community translations on [LyricsTranslate](https://lyricstranslate.com/en/narlan-matos-lyrics.html).
This inventory is being expanded as additional publications and translations are documented.


<!-- add numbers for books and translations based on _data/publications.csv, as follows. 

books in portuguese : n collection = books 

books in other languages: n type = translated_book

anthologies in portuguese: n [collection = anthologies] + [type = bilingual_edition  or translated_anthology AND bilingual_multilingual = TRUE]

anthologies in other languages: n type = bilingual_edition  or translated_anthology-->
---

<table class="language-table">

  <thead>
    <tr>
      <th>Language</th>
      <th style="text-align:center;">Books</th>
      <th style="text-align:center;">Anthologies</th>
      <th style="text-align:center;">Periodicals</th>
      <th style="text-align:center;">Poems on this Website</th>
      <th style="text-align:center;">
        Community Translations<br>
        <small>
          <a href="https://lyricstranslate.com/en/narlan-matos-lyrics.html"
             target="_blank"
             rel="noopener">
            LyricsTranslate
          </a>
        </small>
      </th>
    </tr>
  </thead>

  {% assign languages = site.data.lyrics_translate_languages | sort: "language" %}
  {% assign portuguese = languages | where: "language", "Portuguese" %}

  <!-- Portuguese first -->
  <tbody>

  {% for row in portuguese %}

    {% assign books = 0 %}
    {% assign anthologies = 0 %}

    {% for item in site.data.publications %}

      {% if item.collection == "books" %}
        {% assign books = books | plus: 1 %}
      {% endif %}

      {% if item.collection == "anthologies" %}
        {% assign anthologies = anthologies | plus: 1 %}
      {% endif %}

      {% if item.type == "translated_anthology"
            and (item.bilingual_multilingual == "TRUE"
                 or item.bilingual_multilingual == true) %}
        {% assign anthologies = anthologies | plus: 1 %}
      {% endif %}

    {% endfor %}

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

      <td style="text-align:center;">
        {% if books > 0 %}{{ books }}{% endif %}
      </td>

      <td style="text-align:center;">
        {% if anthologies > 0 %}{{ anthologies }}{% endif %}
      </td>

      <td style="text-align:center;"></td>

      <td style="text-align:center;"></td>

      <td style="text-align:center;">
        {% if row.n_poems %}{{ row.n_poems }}{% endif %}
      </td>

    </tr>

  {% endfor %}

  </tbody>

  <tbody>
    <tr>
      <td colspan="6">
        <hr style="margin:.35em 0;">
      </td>
    </tr>
  </tbody>

  <!-- Other languages -->
  <tbody>

  {% for row in languages %}

    {% unless row.language == "Portuguese" %}

      {% assign books = 0 %}
      {% assign anthologies = 0 %}

      {% for item in site.data.publications %}

        {% assign translated = false %}

        {% assign langs = item.translated_languages | default: "" | split: ";" %}

        {% for lang in langs %}
          {% if lang | strip == row.language %}
            {% assign translated = true %}
          {% endif %}
        {% endfor %}

        {% if translated %}

          {% if item.type == "translated_book" %}
            {% assign books = books | plus: 1 %}
          {% endif %}

          {% if item.type == "translated_anthology" %}
            {% assign anthologies = anthologies | plus: 1 %}
          {% endif %}

        {% endif %}

      {% endfor %}

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

        <td style="text-align:center;">
          {% if books > 0 %}{{ books }}{% endif %}
        </td>

        <td style="text-align:center;">
          {% if anthologies > 0 %}{{ anthologies }}{% endif %}
        </td>

        <td style="text-align:center;"></td>

        <td style="text-align:center;"></td>

        <td style="text-align:center;">
          {% if row.n_poems %}{{ row.n_poems }}{% endif %}
        </td>

      </tr>

    {% endunless %}

  {% endfor %}

  </tbody>

</table>

