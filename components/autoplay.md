---
title: Autoplay
layout: docs.html
slug: autoplay
algolia: true
---

[[lead]]Manages auto-changing of slides after a defined time interval[[/lead]]

## Usage <small>type: `optional`</small>

This module can be imported using `Autoplay` keyword.

```js
import { Glide, Autoplay } from '@glidejs/glide/dist/glide.modular.esm'

new Glide('.glide').mount({ Autoplay })
```

## Properties

### `time` <small>type: `{Number}`</small>

- **Usage:** Holds currently active auto-changing interval time

## Methods

### `mount()`

- **Usage:** Mounts and initializes a component

---

### `start()`

- **Usage:** Starts auto-changing of slides on the instance

### `stop()`

- **Usage:** Stops auto-changing of slides on the instance

---

### `bind()`

- **Usage:** Registers listener for stopping auto-changing on mouseover

---

### `unbind()`

- **Usage:** Removes previously registered mouseover listener