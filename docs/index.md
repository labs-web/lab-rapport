---
layout : default
slug: /index
order : 1
---

<div class="book">
{%- assign chapitres = site.chapitres | sort: "order"  -%}
{% for chapitre in chapitres %}
    <page size="A4">
    {{ chapitre.content }}
    </page>
{%- endfor -%}  
</div>

