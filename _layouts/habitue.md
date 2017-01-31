---
layout: default
---
<h1>{{ page.name }}</h1>
<p>
  <img src="{{ page.photo }}" />
</p>
<p>
  {{ page.zone }}
  {% if page.website %}— <a href="{{ page.website }}">{{ page.website }}</a>{% endif %}

  — <a href="https://twitter.com/@{{ page.twitter }}">@{{ page.twitter }}</a>
</p>

<p>
{{ page.desc }}
</p>

<ul>{% for link_hash in page.links %}<li>
  {% assign url = link_hash[1] %}
  {% assign name = link_hash[0] %}
  <a href={{ url }}>{{ name }}</a>
</li>{% endfor %}</ul>

{{ content }}
