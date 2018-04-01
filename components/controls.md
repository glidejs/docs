---
title: Controls
layout: docs.html
slug: controls
algolia: true
---

[[lead]]Manages creating a buttons that allows user to control movement of the instance[[/lead]]

## Usage <small>type: `optional`</small>

This module can be imported using `Controls` keyword.

```js
import { Glide, Controls } from 'glidejs/dist/glide.modular.esm'

new Glide('.glide').mount({ Controls })
```

## Properties

### `items` <small>type: `{HTMLCollection}`</small>

- **Usage:** Holds collection of `<a>` elements located inside slides

## Methods

### `mount()`

- **Usage:** Mounts and initializes a component

---

### `setActive()`

- **Usage:** Sets an active class to navigation controls

---

### `removeActive()`

- **Usage:** Removes active class from navigation controls

---

### `addClass(controls)`

- **Arguments:**
  - `{HTMLCollection} controls`

- **Usage:** Toggles an active class on a passed collection of HTML elements based on the current index

---

### `removeClass(controls)`

- **Arguments:**
  - `{HTMLCollection} controls`

- **Usage:** Removes an active class from passed collection of HTML elements

---

### `addBindings()`

- **Usage:** Adds click listeners to controls

---

### `removeBindings()`

- **Usage:** Removes click listeners from controls

---

### `bind(elements)`

- **Arguments:**
  - `{HTMLCollection} elements`

- **Usage:** Toggles an active class on a passed collection of HTML elements based on the current index

---

### `unbind(elements)`

- **Arguments:**
  - `{HTMLCollection} elements`

- **Usage:** Removes an active class from passed collection of HTML elements

---

### `click(event)`

- **Arguments:**
  - `{Object} event`

- **Usage:** Control's click event handler which makes movement based on its direction pattern