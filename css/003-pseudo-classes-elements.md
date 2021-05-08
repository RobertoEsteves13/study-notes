# Pseudo Classes

A pseudo class in CSS is a keyword added to represent a special state of the element selected, for example when the link anchor is hovered by the cursor and you want to make it white:

```css
a:hover {
    color: white;
}
```

[See here for a list of all pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

# Pseudo Elements

They are like pseudo-classes, but it represents a specific part of the element, for example to alter only the fist line of the paragraph:

```css
p::first-line {
  color: blue;
  text-transform: uppercase;
}
```

[See here for a list of all pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)
