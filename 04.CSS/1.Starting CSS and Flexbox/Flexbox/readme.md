- Image-Gallery : [image Gallery](./image-gallery.png)

## Mastering FlexBox Like (Never Done Before)

FlexBox (Flexible Box Layout ) is one dimensional modal designed layout to control the flow of items either in row or column by aligning through align-items and justify-content

## Terminology

- Flex container
- Flex Items

1.  The Container properties

| Property        | Value                                                                   | Description                                                                                                               |
| --------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| display         | flex or inline-flex                                                     | to activates flex , display property must need to provide to parent container                                             |
| flex-direction  | row(default), row-reverse column, column-reverse                        | to set define main axis : the primary direction to flow flex items                                                        |
| justify-content | flex-start,flex-end, center, space-between , space-around, space-evenly | to align flex-items in main-axis(horizontally) if direction is row                                                        |
| align-items     | flex-start, flex-end, center, stretch, baseline                         | to align items vertically if direction is row                                                                             |
| flex-wrap       | nowrap(default), wrap, wrap-reverse                                     | either the flex items forced to come in one line(nowrap) or wrap into multiple lines when container's width exceed        |
| align-content   | flex-start, flex-end , center, space-between , space-around, stretch    | it only works when items wrap into multiple lines . it controls the space distribution between wrap items into cross axis |

2.  The Items Properties
    These properties are set on the children elements(Flex Items)

| Property    | Value                                                                   | Description                                                                                                    |
| ----------- | ----------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| order       | 0(default), integer(1, -1, 2)                                           | controls visual order of flex items independent to the source code in HTML, Lower Number comes first           |
| flex-grow   | Number(eg: 1, 0, 2)                                                     | ability to grow flex items if necessary, 1 means items takes remaining space equally, 0(default) it won't grow |
| flex-shrink | Number(1, 0)                                                            | ability to shrink item if necessary, 1(DEFAULT) it shrink, 0 means it won't shrink below the content size      |
| flex-basis  | length (100px, 50%, auto)                                               | default size of element before space is distributed between them (flex-grow) or (flex-shrink)                  |
| flex        | shorthand property for (flex-grow, flex-shrink, flex-basis) eg(1, 1, 0) | combines flex-grow, flex-shrink, and flex-basis in one property                                                |
| align-self  | flex-start, flex-end, center, stretch, baseline                         | overrides the align-items property for this specified items                                                    |

## Understanding the Axes

there is two axes Main axis and cross Axis

1. Main Axis : defined by `flex-direction` (horizontal/row)

- **justify-content** controls the alignment in this axis

2. Cross Axis : The axis perpendicular yo main axis if direction is row (default)

- **align-items** controls the alignment in this axis

| flex-direction | Main Axis(justify-content) | Cross Axis (align-items) |
| -------------- | -------------------------- | ------------------------ |
| row            | Horizontal                 | Verical                  |
| column         | Vertical                   | Horizontal               |

## Some Resources

[css-tricks for flex-box](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

[MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts)

[Visual Tool in codepen](https://codepen.io/enxaneta/full/adLPwv)
