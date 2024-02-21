---
layout: default
chapitre: Utilisation de jekyll
order: 6
---
# Utilisation de jekyll


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

## Références
- [jekyllrb](https://jekyllrb.com/)
- [Liquid filters](https://jekyllrb.com/docs/liquid/filters/)
- [Jekyll cheatsheet](https://devhints.io/jekyll)

