---

title: "Translations by Language"
permalink: /translations/languages/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image

  

---

The table below provides an ongoing inventory of Narlan Matos's work by language,
including original books and their translations, anthologies and translated anthologies,
poetry published in literary journals and other periodicals, individual poems available on this website,
and community translations on [LyricsTranslate](https://lyricstranslate.com/en/narlan-matos-lyrics.html).


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
        Poem Translations on <br>
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

  <!-- Portuguese first -->
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

    <td style="text-align:center;"></td>

    <td style="text-align:center;"></td>

    <td style="text-align:center;"></td>

    <td style="text-align:center;"></td>

    <td style="text-align:center;">
      <strong>{{ row.n_poems }}</strong>
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

  <!-- Remaining languages -->
  <tbody>

  {% assign languages = site.data.lyrics_translate_languages
      | sort: "language" %}

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

      <td style="text-align:center;"></td>

      <td style="text-align:center;"></td>

      <td style="text-align:center;"></td>

      <td style="text-align:center;"></td>

      <td style="text-align:center;">
        {{ row.n_poems }}
      </td>

    </tr>

    {% endunless %}

  {% endfor %}

  </tbody>

</table>

