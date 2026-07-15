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


---

<table class="language-summary">

<thead>
<tr>
  <th>Language</th>
  <th>Books</th>
  <th>Anthologies</th>
  <th>Periodicals</th>
  <th>Poems on this website</th>
  <th>
    Community Translations on
    <a href="https://lyricstranslate.com/en/narlan-matos-lyrics.html"
       target="_blank"
       rel="noopener">
      LyricsTranslate
    </a>
  </th>
</tr>
</thead>

<tbody>

{% assign portuguese = site.data.lyrics_translate_languages
  | where: "language", "Portuguese"
  | first %}

{% if portuguese %}

<tr class="language-native">

<td>
{% if portuguese.slug %}
<a href="{{ '/translations/languages/' | append: portuguese.slug | append: '/' | relative_url }}">
<strong>Portuguese</strong>
</a>
{% else %}
<strong>Portuguese</strong>
{% endif %}
</td>

{% assign books = 0 %}
{% assign anthologies = 0 %}
{% assign poems = 0 %}

{% for item in site.data.publications %}

  {% if item.collection == "books" %}
    {% assign books = books | plus: 1 %}
  {% endif %}

  {% if item.collection == "anthologies" %}
    {% assign anthologies = anthologies | plus: 1 %}
  {% endif %}

  {% if item.type == "translated_anthology"
        and item.bilingual_multilingual == "TRUE" %}
    {% assign anthologies = anthologies | plus: 1 %}
  {% endif %}

{% endfor %}

{% for poem in site.data.poems %}
  {% if poem.language == "Portuguese" %}
    {% assign poems = poems | plus: 1 %}
  {% endif %}
{% endfor %}

<td>{{ books }}</td>
<td>{{ anthologies }}</td>
<td></td>
<td>{{ poems }}</td>
<td>{{ portuguese.n_poems }}</td>

</tr>

{% endif %}

{% assign rows = site.data.lyrics_translate_languages
  | sort: "language" %}

{% for row in rows %}

{% unless row.language == "Portuguese" %}

{% assign books = 0 %}
{% assign anthologies = 0 %}
{% assign poems = 0 %}

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

{% for poem in site.data.poems %}
  {% if poem.language == row.language %}
    {% assign poems = poems | plus: 1 %}
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

<td>{{ books }}</td>
<td>{{ anthologies }}</td>
<td></td>
<td>{{ poems }}</td>
<td>{{ row.n_poems }}</td>

</tr>

{% endunless %}

{% endfor %}

</tbody>

</table>