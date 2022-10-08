# Tailwind CSS Refresher


### My design process:

1. Add the html
2. Layout the things
3. Spacing
4. Box properties (border, background, shadow)
5. Typography
6. Fun element - gradients, circles, backgrounds etc
7. Responsiveness


## Flexbox (CSS)
Properties and values

#### `justify-content` (X axis)
- `flex-start`: Items align to the left side of the container.
- `flex-end`: Items align to the right side of the container.
- `center`: Items align at the center of the container.
- `space-between`: Items display with equal spacing between them.
- `space-around`: Items display with equal spacing around them.

#### `align-items` (Y axis)
- `flex-start`: Items align to the top of the container.
- `flex-end`: Items align to the bottom of the container.
- `center`: Items align at the vertical center of the container.
- `baseline`: Items display at the baseline of the container.
- `stretch`: Items are stretched to fit the container.

#### `flex-direction`
- `row`: Items are placed the same as the text direction.
- `row-reverse`: Items are placed opposite to the text direction.
- `column`: Items are placed top to bottom.
- `column-reverse`: Items are placed bottom to top.
    *Note:*
  - When the `flex-direction` is a `column`, `justify-content` changes to the vertical and `align-items` to the horizontal.
  - When you set the `flex-direction` to a `row-reverse` or `column-reverse`, start and end are also reversed.

#### `order`
- Sometimes reversing the row or column order of a container is not enough. In these cases, we can apply the order property to individual items. **By default, items have a value of 0**, but we can use this property to also set it to a positive or negative integer value (-2, -1, 0, 1, 2).

- Let's say you have three child elements and `.yellow` is the selector for the middle child-element. To reorder the list such that middle element switches it's position with the last element:
```css
.yellow {
    order: 1;
}
```
- `.red` is the selector for the 4th element of 5 child-elements. To reorder the list such that `.red` element takes the first position in the list:
```css
.red {
    order: -3;
}
```

#### `align-self`
-  This property accepts the same values as `align-items` but for a specific element. eg:
```css
.yellow {
    align-self: flex-end;
}
```

#### `flex-wrap`
- `nowrap`: Every item is fit to a single line.
- `wrap`: Items wrap around to additional lines.
- `wrap-reverse`: Items wrap around to additional lines in reverse.
```css
#pond {
    display: flex;
    flex-wrap: wrap; /* spread the elements on to multiple rows */
}
```
- Eg: Wrap the items vertically
```css
#pond {
    display: flex;
    flex-direction: column; /* arrange the flex children elements vertically */
    flex-wrap: wrap; /* spread the elements on to multiple columns */
}
```

#### `flex-flow`
 - The two properties `flex-direction` and `flex-wrap` are used so often together that the shorthand property `flex-flow` was created to combine them. This shorthand property accepts the value of the two properties separated by a space.
 - You can use `flex-flow: row wrap` to set rows and wrap them.
 - Eg: Wrap the items vertically
```css
#pond {
    display: flex;
    flex-flow: column wrap; /* arrange the flex child elements vertically and wrap on to multiple columns */
}
```