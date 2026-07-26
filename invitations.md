---

title: "International Invitations"
permalink: /about/international-invitations/
layout: splash
header:
  overlay_image: /assets/images/header.jpg  # header image


    
---

## International Invitations

The following table lists international literary invitations, residencies, festivals, conferences, and other invited appearances by Narlan Matos.

{% assign invitations = site.data.invitations | sort: "year" | reverse %}

{% if invitations.size > 0 %}

<table class="table table-striped">

<thead>
<tr>
  <th>Year</th>
  <th>Event / Program</th>
  <th>Host Organization</th>
  <th>Location</th>
  <th>Role</th>
  <th>Highlights</th>
</tr>
</thead>

<tbody>

{% for item in invitations %}

<tr>

<td>
{{ item.year }}
</td>

<td>

{% if item.url %}
<a href="{{ item.url | relative_url }}">
<strong>{{ item.title }}</strong>
</a>
{% else %}
<strong>{{ item.title }}</strong>
{% endif %}

{% if item.event and item.event != item.title %}
<br><small>{{ item.event }}</small>
{% endif %}

</td>

<td>
{{ item.organization }}
</td>

<td>

{% if item.city %}
{{ item.city }}
{% endif %}

{% if item.city and item.country %}
,
{% endif %}

{{ item.country }}

</td>

<td>
{{ item.role }}
</td>

<td>

{{ item.description | truncate:120 }}

{% if item.program_pdf %}
<br>
<a href="{{ item.program_pdf | relative_url }}">
Festival program
</a>
{% endif %}

{% if item.video %}
{% if item.program_pdf %} · {% endif %}
<a href="{{ item.video }}">
Video
</a>
{% endif %}

</td>

</tr>

{% endfor %}

</tbody>

</table>

{% else %}

*No invitations have been added yet.*

{% endif %}

