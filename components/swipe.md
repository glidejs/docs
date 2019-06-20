---
title: Swipe
layout: docs.html
slug: swipe
algolia: true
---

[[lead]]Allows for controlling movement of the instance using finger swipe gestures[[/lead]]

## Usage <small>type: `optional`</small>

This module can be imported using `Swipe` keyword.

```js
import Glide, { Swipe } from '@glidejs/glide/dist/glide.modular.esm'

new Glide('.glide').mount({ Swipe })
```

## Methods

### `mount()`

- **Usage:** Mounts and initializes a component. Binds mouse and touch events

---

### `start(event)`

- **Arguments:**
  - `{Object} event`

- **Usage:** Handler of `swipestart` event. Calculates entry points of the user's tap

---

### `move(event)`

- **Arguments:**
  - `{Object} event`

- **Usage:** Handler of `swipemove` event. Calculates user's tap angle and distance

---

### `end(event)`

- **Arguments:**
  - `{Object} event`

- **Usage:** * Handler of `swipeend` event. Finishes user's tap and decides about instance movement

---

### `touches(event)`

- **Arguments:**
  - `{Object} event`

- **Usage:** Normalizes event's touches points according to different types

---

### `threshold(event)`

- **Arguments:**
  - `{Object} event`

- **Usage:** Gets value of minimum swipe distance setting based on event type

---

### `bindSwipeStart()`

- **Usage:** Adds listener for swipe starting event

---

### `unbindSwipeStart()`

- **Usage:** Removes previously added listener for swipe starting event

---

### `bindSwipeMove()`

- **Usage:** Adds a listener for swipe moving event

---

### `unbindSwipeMove()`

- **Usage:** Removes previously added listener for swipe moving event

---

### `bindSwipeEnd()`

- **Usage:** Adds listener for swipe end event

---

### `unbindSwipeEnd()`

- **Usage:** Removes previously added listener for swipe end event

---

### `enable()`

- **Usage:** Enables instance swiping events

---

### `disable()`

- **Usage:** Disables instance swiping events
