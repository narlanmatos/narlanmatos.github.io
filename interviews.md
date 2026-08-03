---
title: "Interviews & Media"
permalink: /reception/interviews/
layout: single
classes: wide
header:
  overlay_image: /assets/images/header.jpg  # header image
---

*Interviews, conversations, and media appearances, conducted in multiple countries and languages, provide a more personal perspective on Narlan Matos's literary work, artistic influences, and intellectual life.* 

*As the archive grows, this page will also include recorded interviews, festival conversations, podcasts, and documentary material.*

---

## Interviews

{% assign interviews = site.data.reception
  | where: "heading", "Interviews & Media"
  | sort: "year"
  | reverse %}

{% if interviews.size > 0 %}

{% for item in interviews %}

{% for item in interviews %}

### {{ item.title }}

<p>

{% if item.authors %}
<em>{{ item.authors }}</em>.
{% endif %}

{% if item.publication %}
<strong>{{ item.publication }}</strong>
{% endif %}

{% if item.country %}
({{ item.country }})
{% endif %}

{% if item.year %}
, {{ item.year }}
{% endif %}

{% if item.language %}
 · {{ item.language }}
{% endif %}

</p>

{% if item.description %}
{{ item.description }}
{% endif %}

<p>

{% assign separator = false %}

{% if item.url %}
<a href="{{ item.url }}" target="_blank" rel="noopener">Online</a>
{% assign separator = true %}
{% endif %}

{% if item.local_copy %}
{% if separator %} | {% endif %}
<a href="{{ item.local_copy | relative_url }}" target="_blank">Archived PDF</a>
{% assign separator = true %}
{% endif %}

{% if item.worldcat_link %}
{% if separator %} | {% endif %}
<a href="{{ item.worldcat_link }}" target="_blank" rel="noopener">WorldCat</a>
{% endif %}

</p>

{% unless forloop.last %}
<hr>
{% endunless %}

{% endfor %}
---

{% endfor %}

{% else %}

No interviews have been added yet.

{% endif %}