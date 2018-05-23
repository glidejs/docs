---
title: Anchors
layout: docs.html
slug: anchors
algolia: true
---

[[lead]]Handles clicking and dragging events of the internal `<a>` HTML elements, so they won't interfere while interacting with an instance[[/lead]]

## Usage <small>type: `optional`</small>

This module can be imported using `Anchors` keyword.

```js
import Glide, { Anchors } from '@glidejs/glide/dist/glide.modular.esm'

new Glide('.glide').mount({ Anchors })
```

## Properties

### `items` <small>type: `{HTMLCollection}`</small>

- **Usage:** Holds collection of `<a>` elements located inside slides

## Methods

### `mount()`

- **Usage:** Mounts and initializes a component

---

### `detach()`

- **Usage:** Detaches `href` attribute from anchors and prevents redirections after click or swipe

---

### `attach()`

- **Usage:** Restores `href` attribute on anchors and allows for redirections on click