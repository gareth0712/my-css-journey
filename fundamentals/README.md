# Fundamentals

## Box sizing

- By default, box-sizing is set to `content-box`, not `border-box`.
- Content-box: when you set component A of width 100px with 10px padding, that 10px padding will extend the width of component A, resulting in width of 120px.
- Border-box: Following the above example, component A will still have width of 100px with `box-sizing: border-box;`
- We always set `box-sizing: border-box;` as default by:

```
*, *::before, *::after {
  box-sizing: border-box;
}
```

- The best practice would be using the following (Reference: https://css-tricks.com/inheriting-box-sizing-probably-slightly-better-best-practice/) so that when you want to set to use `content-box` explicitly, it won't be overridden.

```
html {
  box-sizing: border-box;
}
*, *:before, *:after {
  box-sizing: inherit;
}
```

## Horizontally center an item

- Set the margin of left and right to auto by e.g. `margin: 0 auto;`
- Setting the width of the element will prevent it from stretching out to the edges of its container.
- The element will then take up the specified width, and the remaining space will be split equally between the two margins:
