# What is CSS

  CSS (Cascading Style Sheet) is a style language used to give on HTML and XML documents and it describes how the document will appear on the screen visually, like colors, layouts and even animations.

# Syntax

  The syntax of CSS is represented as follow:

```css
/* A rule consists of some parts */
h1 /* Selector */ { 
  /*property: declaration */
    color   : red;
}
```

# Selectors

  Selectors are used to define what elements of the HTML will apply the rule. It can be HTML elements, classes, ID's, attributes and universally. Note that the latter is mostly discouraged to use since it causes unecessary overhead by **checking every single HTML element on your document**, so you should use the `body` HTML instead unless there's no other choice.

```css
/* Selecting a HTML element */
h1 { ... }

/* Selecting a class */
.class { ... }
/* Selecting an ID */
#id { ... }

/* Selecting an attribute */
[disabled] { ... }

/* Selecting everything (NOTE: Use body HTML element if possible */
* {}
```

# Properties and values

  Properties are selector's characteristics that determine the way it will be displayed on the screen, and we assign values to them. Each property has a type of value that is valid.

```css
h1 {
  font-family: sans-serif;
  color: red;
  background: #AAAAAA;
  font-size: 1.2em;
}
```

# Cascading

  As CSS being cascading, selecting a single element doesn't mean it will affect other elements besides the one being selected. Because elements can contain inner elements, they will have the style applied. Think it's something like inheritance, as the father element rule will influence his sons.

```html
<style>
  section {
    background: red;
    color: white;
  }
</style>

<body>
  <section>
    <h1>This element is influenced by the section rules</h1>
  </section>
    <h1>And this one isn't!</h1>
</body>
```

## Priority

  Rules can be overiden by other rules that's more specific to the element, and the order, from the most to the least specific, is:

```
Inline Styles > #ID > .class || :pseudo-class || [attribute] > HTML elements || ::pseudo-element
```

# Combinators

  They can be used to combine multiple elements to follow a single rule only applied to them. There are four combinators that can be used:

* General Sibling: Elements share the same parent **AND** second element comes after first element. Ex:`h2 ~ p`
* Adjacent Sibling: Elements share the same parent **AND** second element comes **immediately** after fist element. Ex:`h2 + p`
* Child: Second element is a direct child of first element. Ex:`div > p`
* Descendant: Second element is a descendant of the first element. Ex:`div p`