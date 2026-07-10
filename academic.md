---

title: "Academic Studies"
permalink: /reception/criticism/academic/
layout: single
header:
  overlay_image: /assets/images/header.jpg  # header image

feature_row:
  - image_path: /assets/images/portraits/guara-cover.jpg
    title: "Scholarly Dossier: Guará – Revista de Linguagem e Literatura"
    excerpt: "A special issue devoted entirely to the poetry and poetics of Narlan Matos, bringing together essays, articles, and reflections on his work across themes of language, memory, identity, and literary reinvention."
    url: "/reception/criticism/academic/guara-dossier.md/"
    btn_label: "View Dossier"
    btn_class: "btn--primary"
    
---

## Featured Collection
{% include feature_row id="feature_row" %}

## All Academic Studies

{% assign items = site.data.reception | where: "type", "academic" %}

{% for item in items %}

### {{ item.title }}

{% if item.authors %}
**{{ item.authors }}**  
{% endif %}

{% if item.publication %}
*{{ item.publication }}*{% if item.year %} ({{ item.year }}){% endif %}  
{% endif %}

{% if item.language %}
Language: {{ item.language }}  
{% endif %}

{% if item.doi %}
DOI:
<a href="https://doi.org/{{ item.doi }}" target="_blank" rel="noopener">
{{ item.doi }}
</a>
{% endif %}

{% if item.related_work %}
<br>
Related work: {% if item.related_work_url %}<a href="{{ item.related_work_url | relative_url }}"><em>{{ item.related_work }}</em></a>{% else %}<em>{{ item.related_work }}</em>{% endif %}
{% endif %}

{% if item.url %}
<br>
<a href="{{ item.url }}" target="_blank" rel="noopener">Read online</a>{% if item.local_copy %}&nbsp;&nbsp;{% endif %}
{% endif %}
{% if item.local_copy %}
<a href="{{ item.local_copy | relative_url }}" target="_blank" rel="noopener">View archived copy</a>
{% endif %}

---

{% endfor %} 