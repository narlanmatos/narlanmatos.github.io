---

title: "Translations by Language"
permalink: /translations/languages/
layout: single
header:
  overlay_image: /assets/images/header.jpg  # header image

  

---

The table below summarizes the languages into which Narlan Matos's work has been translated or published.
It includes books, anthologies, poetry published in literary journals and other periodicals, individual poems available on this website, and community translations on [LyricsTranslate](https://lyricstranslate.com/en/narlan-matos-lyrics.html).
This inventory is being expanded as additional publications and translations are documented.

<!--modify the script so that (1) the hyperlink for lyricstranslate is only on the word "LyricsTranslate", and (2) there are hyperlinks on the n books and n anthologies in portuguese to /poetry/books/ and /poetry/anthologies/, respectively, and also from n poems on this website to /poetry/selected-poems/-->

<table class="language-table">

<thead>
<tr>
  <th>Language</th>
  <th style="text-align:center;">Books</th>
  <th style="text-align:center;">Anthologies</th>
  <th style="text-align:center;">Periodicals</th>
  <th style="text-align:center;">Poems on this website</th>
  <th style="text-align:center;">
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

{% assign portuguese = site.data.language_statistics
   | where: "language", "Portuguese" %}

{% for row in portuguese %}

<tr style="border-bottom:2px solid #bbb;">

<td>

{% if row.slug and row.slug != "" %}
<a href="{{ '/translations/languages/' | append: row.slug | append: '/' | relative_url }}">
<strong>{{ row.language }}</strong>
</a>
{% else %}
<strong>{{ row.language }}</strong>
{% endif %}

</td>

<td align="center">
{% unless row.n_books == 0 or row.n_books == "0" %}
{{ row.n_books }}
{% endunless %}
</td>

<td align="center">
{% unless row.n_anthologies == 0 or row.n_anthologies == "0" %}
{{ row.n_anthologies }}
{% endunless %}
</td>

<td align="center">
{% unless row.n_periodicals == 0 or row.n_periodicals == "0" %}
{{ row.n_periodicals }}
{% endunless %}
</td>

<td align="center">
{% unless row.n_poems == 0 or row.n_poems == "0" %}
{{ row.n_poems }}
{% endunless %}
</td>

<td align="center">
{% unless row.n_poems_LyricsTranslate == 0 or row.n_poems_LyricsTranslate == "0" %}
{{ row.n_poems_LyricsTranslate }}
{% endunless %}
</td>

</tr>

{% endfor %}

{% assign languages = site.data.language_statistics
   | where_exp: "item", "item.language != 'Portuguese'"
   | sort: "language" %}

{% for row in languages %}

<tr>

<td>

{% if row.slug and row.slug != "" %}
<a href="{{ '/translations/languages/' | append: row.slug | append: '/' | relative_url }}">
{{ row.language }}
</a>
{% else %}
{{ row.language }}
{% endif %}

</td>

<td align="center">
{% unless row.n_books == 0 or row.n_books == "0" %}
{{ row.n_books }}
{% endunless %}
</td>

<td align="center">
{% unless row.n_anthologies == 0 or row.n_anthologies == "0" %}
{{ row.n_anthologies }}
{% endunless %}
</td>

<td align="center">
{% unless row.n_periodicals == 0 or row.n_periodicals == "0" %}
{{ row.n_periodicals }}
{% endunless %}
</td>

<td align="center">
{% unless row.n_poems == 0 or row.n_poems == "0" %}
{{ row.n_poems }}
{% endunless %}
</td>

<td align="center">
{% unless row.n_poems_LyricsTranslate == 0 or row.n_poems_LyricsTranslate == "0" %}
{{ row.n_poems_LyricsTranslate }}
{% endunless %}
</td>

</tr>

{% endfor %}

</tbody>

</table>