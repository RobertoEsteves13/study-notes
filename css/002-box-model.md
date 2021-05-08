# Box Model

Every element in HTML is interpreted as a box by CSS, which they have their own margin, border, padding and content. From outer to inner:

- Margin is the distance between two different HTML elements, outside the box

- Border is self explanatory

- Padding is the distance between the content and the box, it only affects elements that are inside

- Content is the elements or the actual content (like text and images)

## Margin Collapsing

If elements are next to each other, it will collapse the margin of the element having it's lowest value so only the biggest margin will be applied. This is automatically done so elements don't have a huge space between them. 

This can be noticed on elements that are adjacents or on a parent with children that have a margin. If the parent element has padding, inline content (other than the child 
elements) or a border, this behavior should not occur, the child margin 
will instead be added to the content of the wrapping parent element.
