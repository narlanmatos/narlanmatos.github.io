---
title: "Interviews & Media"
permalink: /reception/interviews/
layout: single
classes: wide
header:
  overlay_image: /assets/images/header.jpg  # header image
---

Interviews, conversations, and media appearances provide a more personal perspective on Narlan Matos's literary work, artistic influences, and intellectual life. Conducted in multiple countries and languages, these conversations document his reflections on poetry, translation, exile, Brazilian and international literature, and the cultural contexts in which his work has been received.

As the archive grows, this page will also include recorded interviews, festival conversations, podcasts, and documentary material.

---

## Interviews

{% assign interviews = site.data.reception
  | where: "heading", "Interviews & Media"
  | sort: "year"
  | reverse %}

{% if interviews.size > 0 %}

{% for item in interviews %}

### {{ item.title }}

{% if item.authors %}
**Interviewer:** {{ item.authors }}

{% endif %}

{% if item.publication %}
**Publication:** *{{ item.publication }}*
{% endif %}

{% if item.year %}
({{ item.year }})
{% endif %}

{% if item.language %}
<br>**Language:** {{ item.language }}
{% endif %}

{% if item.description %}

{{ item.description }}

{% endif %}

{% assign separator = false %}

{% if item.url or item.local_copy or item.worldcat_link %}

<p>

{% if item.url %}
<a href="{{ item.url }}" target="_blank" rel="noopener">Online version</a>
{% assign separator = true %}
{% endif %}

{% if item.local_copy %}
{% if separator %} &nbsp;|&nbsp; {% endif %}
<a href="{{ item.local_copy | relative_url }}" target="_blank" rel="noopener">Archived copy</a>
{% assign separator = true %}
{% endif %}

{% if item.worldcat_link %}
{% if separator %} &nbsp;|&nbsp; {% endif %}
<a href="{{ item.worldcat_link }}" target="_blank" rel="noopener">WorldCat</a>
{% endif %}

</p>

{% endif %}

---

{% endfor %}

{% else %}

No interviews have been added yet.

{% endif %}