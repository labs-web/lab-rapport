---
layout : default
order : 2
---

# Utilisation de Jekyll

## Installation 

<!-- TODO : Procédure d'installation de Jekyll -->

## Exemple de création d'un site web 

Création d'un nouveau site web

```bash
jekyll new my-awesome-site

```

Exécution de site web

```bash
bundle exec jekyll serve
```

## Utilisation 

### Relative URL

```conf
{{ "/assets/style.css" | relative_url }}

/my-baseurl/assets/style.css

```

### Markdownify

Convert a Markdown-formatted string into HTML.

```conf
{{ page.excerpt | markdownify }}
```

# Références
- [jekyllrb](https://jekyllrb.com/)
- [Liquid filters](https://jekyllrb.com/docs/liquid/filters/)