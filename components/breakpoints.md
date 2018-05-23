---
title: Breakpoints
layout: docs.html
slug: breakpoints
algolia: true
---

[[lead]]Reconfigures instance and its options based on currently matched `@media` breakpoint[[/lead]]

## Usage <small>type: `optional`</small>

This module can be imported using `Breakpoints` keyword.

```js
import Glide, { Breakpoints } from '@glidejs/glide/dist/glide.modular.esm'

new Glide('.glide').mount({ Breakpoints })
```

## Methods

### `match(breakpoints)`

- **Arguments:**
  - `{Object} breakpoints`

- **Usage:** Matches currently active `@media` breakpoint from the passed collection and returns configured settings object for that size

```js
// Return `{ perView: 1 }` with assumptions
// that width of the window is <=600px.
Breakpoints.match({
  600: { perView: 1 },
  1200: { perView: 3 }
})
```
