---

title: "Academic Studies"
permalink: /reception/criticism/academic/
layout: single
header:
  overlay_image: /assets/images/header.jpg  # header image

feature_row:
  - image_path: /assets/images/criticism/guara-cover.jpg
  - excerpt: "A special issue devoted entirely to the poetry and poetics of Narlan Matos, bringing together essays, articles, and reflections on his work across themes of language, memory, identity, and literary reinvention."
  - url: "https://seer.pucgoias.edu.br/index.php/guara/issue/view/488"
    btn_label: "View Dossier"
    btn_class: "btn--primary"
    
---

# Scholarly Dossier: *Guará – Revista de Linguagem e Literatura*
{% include feature_row id="feature_row" %}

# All Academic Studies

{% assign items = site.data.reception | where: "type", "academic" %}

{% for item in items %}

<p>
<strong>{{ item.title }}</strong><br>

{% if item.authors %}
{{ item.authors }}.
{% endif %}

{% if item.publication %}
<em>{{ item.publication }}</em>{% if item.volume %} {{ item.volume }}{% endif %}{% if item.issue %}({{ item.issue }}){% endif %}{% if item.pages %}, {{ item.pages }}{% endif %}{% if item.year %}, {{ item.year }}{% endif %}.
{% endif %}

{% if item.language %}
({{ item.language }})
{% endif %}
</p>

{% if item.related_work %}
<p>
Related work:
{% if item.related_work_url %}
<a href="{{ item.related_work_url | relative_url }}"><em>{{ item.related_work }}</em></a>
{% else %}
<em>{{ item.related_work }}</em>
{% endif %}
</p>
{% endif %}

{% if item.doi %}
<p>
DOI:
<a href="https://doi.org/{{ item.doi }}" target="_blank" rel="noopener">
{{ item.doi }}
</a>
</p>
{% endif %}

{% if item.url or item.local_copy %}
<p>
{% if item.url %}
<a href="{{ item.url }}" target="_blank" rel="noopener">Online version</a>
{% endif %}

{% if item.url and item.local_copy %}
&nbsp; | &nbsp;
{% endif %}

{% if item.local_copy %}
<a href="{{ item.local_copy | relative_url }}" target="_blank" rel="noopener">Archived copy</a>
{% endif %}
</p>
{% endif %}

<hr>

{% endfor %}