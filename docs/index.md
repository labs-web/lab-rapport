---
layout: default
order: 1
---
{{page.url}}

{% assign pages = site.pages | sort: "order" %}
{% for page in pages %}
{% if page.url != "/feed.xml" 
and page.url != "/assets/css/style.css" 
and  page.url != "/"  
and page.url != "/presentation.html" %}

<!-- page.content | markdownify -->

{% include eval.liquid content=page.content %}
 {{page.content | markdownify}}


{% endif %}
{% endfor %}



 
 
