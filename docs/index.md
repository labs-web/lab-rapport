---
layout : default
slug: /index
order : 1
---

# Rapport 

{%- assign chapitres = site.chapitres | sort: "order"  -%}
{% for chapitre in chapitres %}
    <article>
        {{ chapitre.content }}
    </article>
     <article>
        {{ chapitre.content | markdownify }}
    </article>
{%- endfor -%}