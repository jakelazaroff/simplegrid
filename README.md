# simplegrid

**Simplegrid** is a lightweight grid system built with SCSS.

## Documentation

### Functions

- ```rows($rows)``` — outputs the height of the supplied number of rows in pixels. Defaults to 1.
- ```columns($columns)``` — outputs the width of the supplied number of columns in vw. Defaults to 1.

### Mixins

- ```rem($property, $value)``` — outputs the supplied property with the value converted to rem, with a fallback of the equivalent value in pixels.
- ```breakpoint($size)``` — for a string key in the $queries variable, outputs a media query with that key's minimum width value in rem, with all the column calculations based on that key's column count.

### Variables

Simplegrid defines a number of variables that can be overridden by declaring them before including ```grid.scss```.

- ```$column-count``` — the number of columns at the smallest breakpoint. Defaults to 4.
- ```$gutter``` — the gutter on each side of a column, in pixels. Included in column width. Defaults to 10px.
- ```$row-height``` — the height of a grid row. Usually, a line of text will take up multiple grid rows. Defaults to 4px.
- ```$type-ratio``` — the ratio of 10px to 1em at the default browser font size. Under normal circumstances, shouldn't need to be overridden. Defaults to .625.
- ```$default-media-property``` — the default property if omitted from the @media mixin. Defaults to min-width.

In addition, Simplegrid allows you to map breakpoint strings to pixel values. This takes the form of

```scss
$queries: (
    "small": (480px, $column-count * 2),
    "medium": (720px, $column-count * 3),
    "large": (960px, $column-count * 3)
)
``` 

and can also be overridden.
