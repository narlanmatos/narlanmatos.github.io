---

title: "Translations by Language"
permalink: /translations/languages/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image

  
    
---

*This page links to translations and bilingual editions by language. Entries include original books, anthologies, periodical publications, translations of individual poems, and festival publications or recordings.*

## Languages

## Languages

<table>

<thead>
<tr>
  <th>Language</th>
  <th>Books</th>
  <th>Anthologies</th>
  <th>Periodicals</th>
  <th>Poem Translations</th>
  <th>LyricsTranslate</th>
  <th>Performances</th>
</tr>
</thead>

<tbody>

{% assign languages = site.data.lyrics_translate_languages | sort: "language" %}

{% for row in languages %}

{% assign language = row.language | strip %}

{% assign books = 0 %}
{% assign anthologies = 0 %}
{% assign periodicals = 0 %}
{% assign poems = 0 %}
{% assign performances = 0 %}

{% for publication in site.data.publications %}

  {% assign found = false %}

  {% for field in "original_languages|translated_languages|publication_languages" | split:"|" %}

    {% assign value = publication[field] %}

    {% if value %}

      {% assign values = value | split:";" %}

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

      {% when "performances" %}
        {% assign performances = performances | plus: 1 %}

    {% endcase %}

  {% endif %}

{% endfor %}

<tr>

<td>

{% if row.has_page == "TRUE" %}
<a href="{{ '/translations/languages/' | append: (language | slugify) | append:'/' | relative_url }}">
{{ language }}
</a>
{% else %}
{{ language }}
{% endif %}

</td>

<td>{{ books }}</td>
<td>{{ anthologies }}</td>
<td>{{ periodicals }}</td>
<td>{{ poems }}</td>
<td>{{ row.n_poems | default: 0 }}</td>
<td>{{ performances }}</td>

</tr>

{% endfor %}

</tbody>

</table>

