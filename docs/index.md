---
layout : default
slug: /index
order : 1
---

# Rapport 

{%- assign chapitres = site.chapitres | sort: "order"  -%}
{% for chapitre in chapitres %}
<page size="A4">
  {{ chapitre.content }}
<page>
<page size="A4">
  {{ chapitre.content | markdownify }}
<page>
{%- endfor -%}