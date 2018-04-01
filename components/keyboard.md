---
title: Keyboard
layout: docs.html
slug: keyboard
algolia: true
---

[[lead]]Allows for controlling movement of the instance with keyboard's arrow keys[[/lead]]

## Usage <small>type: `optional`</small>

This module can be imported using `Keyboard` keyword.

```js
import { Glide, Keyboard } from 'glidejs/dist/glide.modular.esm'

new Glide('.glide').mount({ Keyboard })
```

## Methods

### `mount()`

- **Usage:** Mounts and initializes a component. Creates event listeners for keyboard key presses

---

### `bind()`

- **Usage:** Binds `keyup` event listener for key presses

---

### `unbind()`

- **Usage:** Removes previously added `dragstart` event

---

### `press(event)`

- **Arguments:**
  - `{Object} event`

- **Usage:** `keyup` event handler. Makes movement base on arrow key direction