---

title: "Academic Studies"
permalink: /reception/criticism/academic-studies/
layout: single
header:
  overlay_image: /assets/images/header.jpg  # header image


    
---

{% assign items = site.data.reception | where: "type", "academic" %}

{% for item in items %}

### {{ item.title }}

{% if item.image %}
<figure class="align-center">
  <img src="{{ item.image | relative_url }}" alt="{{ item.title }}">
</figure>
{% endif %}

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