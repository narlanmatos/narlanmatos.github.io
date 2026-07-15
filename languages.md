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



{% assign portuguese = site.data.language_statistics
  | where: "language", "Portuguese" %}

{% assign other_languages = site.data.language_statistics
  | where_exp: "item", "item.language != 'Portuguese'"
  | sort: "language" %}

| Language | Books | Anthologies | Periodicals | Poems on this website | Community Translations on <a href="https://lyricstranslate.com/en/narlan-matos-lyrics.html" target="_blank" rel="noopener">LyricsTranslate</a> |
|:---------|------:|------------:|------------:|----------------------:|--------------------------------------:|
{% for row in portuguese %}
| **{% if row.slug != "" %}[{{ row.language }}]({{ '/translations/languages/' | append: row.slug | append: '/' | relative_url }}){% else %}{{ row.language }}{% endif %}** | {% unless row.n_books == "0" or row.n_books == 0 %}{{ row.n_books }}{% endunless %} | {% unless row.n_anthologies == "0" or row.n_anthologies == 0 %}{{ row.n_anthologies }}{% endunless %} | {% unless row.n_periodicals == "0" or row.n_periodicals == 0 %}{{ row.n_periodicals }}{% endunless %} | {% unless row.n_poems == "0" or row.n_poems == 0 %}{{ row.n_poems }}{% endunless %} | {% unless row.n_poems_LyricsTranslate == "0" or row.n_poems_LyricsTranslate == 0 %}{{ row.n_poems_LyricsTranslate }}{% endunless %} |
{% endfor %}
| | | | | | |
{% for row in other_languages %}
| {% if row.slug != "" %}[{{ row.language }}]({{ '/translations/languages/' | append: row.slug | append: '/' | relative_url }}){% else %}{{ row.language }}{% endif %} | {% unless row.n_books == "0" or row.n_books == 0 %}{{ row.n_books }}{% endunless %} | {% unless row.n_anthologies == "0" or row.n_anthologies == 0 %}{{ row.n_anthologies }}{% endunless %} | {% unless row.n_periodicals == "0" or row.n_periodicals == 0 %}{{ row.n_periodicals }}{% endunless %} | {% unless row.n_poems == "0" or row.n_poems == 0 %}{{ row.n_poems }}{% endunless %} | {% unless row.n_poems_LyricsTranslate == "0" or row.n_poems_LyricsTranslate == 0 %}{{ row.n_poems_LyricsTranslate }}{% endunless %} |
{% endfor %}