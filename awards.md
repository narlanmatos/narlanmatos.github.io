---

title: "Awards & Honors"
permalink: /about/awards/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image


    
---

---
title: "Awards"
permalink: /awards/
layout: single
---

# Awards

{% assign awards = site.data.awards | sort: "year" | reverse %}

<table>
<thead>
<tr>
<th>Work</th>
<th>Award</th>
<th>Recipient</th>
<th>Organization</th>
<th>Year</th>
<th>Country</th>
<th>Category</th>
<th>Status</th>
</tr>
</thead>

<tbody>

{% for item in awards %}

<tr>

<td>
{% if item.title_url %}
<a href="{{ item.title_url | relative_url }}">
{{ item.title }}
</a>
{% else %}
{{ item.title }}
{% endif %}
</td>

<td>
{{ item.award }}
</td>

<td>
{{ item.award_recipient }}
</td>

<td>
{{ item.organization }}
</td>

<td>
{{ item.year }}
</td>

<td>
{{ item.country }}
</td>

<td>
{{ item.category }}
</td>

<td>
{{ item.status }}
</td>

</tr>

{% endfor %}

</tbody>
</table>