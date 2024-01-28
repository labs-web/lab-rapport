---
layout : default
slug: /index
order : 1
---

<div class="book">
{%- assign pages = site.pages | sort: "order"  -%}
{% for page in pages %}
<article size="A4">
    {{ page.content }}
</article>
{% endfor %}  
</div>

