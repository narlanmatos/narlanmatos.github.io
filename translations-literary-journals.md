---

title: "Translations in Literary Journals and Other Publications"
permalink: /translations/translations-literary-journals/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image


---


{% assign journal_translations = site.data.publications
  | where: "collection", "periodicals"
  | where: "type", "literary_journal"
  | where_exp: "item", "item.publication_languages != 'Portuguese'"
  | sort: "publication_date"
  | reverse
%}

{% for item in journal_translations %}
<p><strong>{{ item.publication_date }}</strong><br>
{%- if item.url -%}
<a href="{{ item.url | relative_url }}"><em>{{ item.full_title | default: item.title }}</em></a>
{%- else -%}
<em>{{ item.full_title | default: item.title }}</em>
{%- endif -%}
{%- if item.authors -%}. {{ item.authors }}{%- endif -%}
{%- if item.translated_languages -%}. {{ item.translated_languages }}{%- endif -%}
{%- if item.translators -%}. Translated by {{ item.translators }}{%- endif -%}
{%- if item.publisher -%}. <em>{{ item.publisher }}</em>{%- endif -%}
{%- if item.volume -%}: {{ item.volume }}{%- endif -%}
{%- if item.issue -%}({{ item.issue }}){%- endif -%}
{%- if item.pages -%}, {{ item.pages }}{%- endif -%}
{%- if item.publication_place -%}. {{ item.publication_place }}{%- endif -%}
{%- if item.edition -%}. {{ item.edition }}{%- endif -%}
{%- if item.isbn -%}. ISBN {{ item.isbn }}{%- endif -%}
{%- if item.issn -%}. ISSN {{ item.issn }}{%- endif -%}
{%- if item.worldcat_link -%} · <a href="{{ item.worldcat_link }}" target="_blank" rel="noopener">WorldCat</a>{%- endif -%}
{%- if item.read_link -%} · <a href="{{ item.read_link }}" target="_blank" rel="noopener">Read</a>{%- endif -%}
{%- if item.local_copy -%} · <a href="{{ item.local_copy | relative_url }}" target="_blank" rel="noopener">Archived Copy</a>{%- endif -%}
</p>
{% endfor %}