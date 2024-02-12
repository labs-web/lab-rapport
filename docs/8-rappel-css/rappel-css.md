# Rappel CSs

## Pseudo-classes


### :first-child

The :first-child CSS pseudo-class represents the first element among a group of sibling elements.

```css

li:first-child {
  border: 2px solid orange;
}

```

### :first-of-type

```css
dt {
  font-weight: bold;
}

dd {
  margin: 3px;
}

dd:first-of-type {
  border: 2px solid orange;
}


```

### :has()

- https://developer.mozilla.org/en-US/docs/Web/CSS/:has


```css
/* Selects an h1 heading with a
paragraph element that immediately follows
the h1 and applies the style to h1 */
h1:has(+ p) {
  margin-bottom: 0;
}

```

#### Logical operations

```css
body:has(video):has(audio) {
  /* styles to apply if the content contains both audio AND video */
}

```




# Références
- [](https://developer.mozilla.org/en-US/docs/Web/CSS/)