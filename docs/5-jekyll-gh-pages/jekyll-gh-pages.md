---
layout: default
order: 5
---
# Configuration de jekyll avec github page

### GITHUB-PAGES-VERSION

- https://pages.github.com/versions/
- github-pages	229

## Création de site web
```bash
jekyll new --skip-bundle .

```

## Configuration de Gemfile 

```ruby
# gem "jekyll", "~> 4.3.3"
gem "github-pages", "~> 229", group: :jekyll_plugins
```

## Installation de jekyll 

```bash
bundle install
```

## Erreur 


```
<internal:C:/Ruby32-x64/lib/ruby/3.2.0/rubygems/core_ext/kernel_require.rb>:38:in `require': cannot load such file -- webrick (LoadError)
        from <internal:C:/Ruby32-x64/lib/ruby/3.2.0/rubygems/core_ext/kernel_require.rb>:38:in 
```
### Solution 

- https://github.com/jekyll/jekyll/issues/8523

```bash
bundle add webrick
```

