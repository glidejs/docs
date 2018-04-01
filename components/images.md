---
title: Images
layout: docs.html
slug: images
algolia: true
---

[[lead]]Handles dragging events of the internal `<img>` HTML elements, so they won't interfere while interacting with an instance[[/lead]]

## Usage <small>type: `optional`</small>

This module can be imported using `Images` keyword.

```js
import { Glide, Images } from 'glidejs/dist/glide.modular.esm'

new Glide('.glide').mount({ Images })
```

## Methods

### `mount()`

- **Usage:** Mounts and initializes a component. Creates event listeners for `<img>` elements

---

### `bind()`

- **Usage:** Binds `dragstart` event to prevent dragging on images

---

### `unbind()`

- **Usage:** Removes previously added `dragstart` event

---

### `press(event)`

- **Arguments:**
  - `{Object} event`

- **Usage:** `keyup` event handler. Prevents dragging on images