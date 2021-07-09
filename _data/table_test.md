---
title: Table test
---

<table>
  {% for row in site.data.authors %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>

{% assign row = site.data.authors[0] %}
{{ row | inspect }}

{
  "First name"=>"John",
  "Last name"=>"Doe",
  "Age"=>"35",
  "Location"=>"United States"
}

{{ row["First name"] }}
{{ row["Last name"] }}

{% assign row = site.data.authors[0] %}
{% for pair in row %}
  {{ pair | inspect }}
{% endfor %}

["First name", "John"]
["Last name", "Doe"]
["Age", "35"]
["Location", "United States"]