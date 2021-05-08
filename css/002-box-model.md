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

## Box sizing

By default, if you set the box's width and height, it will only apply to the content of the box. This is bad cause it doesn't account for padding and border of the box, and if setting that elements explicitely can break the layout of the site. To make the box size account for the padding and border, do `box-sizing: border-box`.

**Tip:** Set using the universal selector cause it will not inherit but **overwrite all elements of the HTML**

```css
* {
    box-sizing: border-box;
}
```

# Display property

In CSS, we can change how elements should be displayed on the page using the `display` property. There are some main values that you can put on display:

| Value          | Meaning                                                                                                                                                                                         |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `none`         | Nothing will be displayed                                                                                                                                                                       |
| `inline`       | The element generates one or more inline element boxes that do not generate line breaks before or after themselves. In normal flow, the next element will be on the same line if there is space |
| `block`        | The element generates a block element box, generating line breaks both before and after the element when in the normal flow.                                                                    |
| `inline-block` | The element generates a block element box that will be flowed with surrounding content as if it were a single inline box (behaving much like a replaced element would).                         |

**Note:** `inline-block` is the same as `inline flow-root`
