---
title: Transition
layout: docs.html
slug: transition
algolia: true
---

[[lead]]Controls transition durations of the instance[[/lead]]

## Usage <small>type: `required`</small>

This module is requisite and it's imported within a bundle.

## Properties

### `duration` <small>type: `{Number}`</small>

- **Usage:** Holds duration of the transition based on currently running animation type

## Methods

### `compose(property)`

- **Arguments:**
  - `{String} property`

- **Usage:** Returns a value of CSS transition property based on duration

---

### `set(property)`

- **Arguments:**
  - `{String} property`

- **Usage:** Applies transition declaration to wrapper HTML element

---

### `remove()`

- **Usage:** Clears transition declarations from wrapper HTML element

---

### `after(callback)`

- **Arguments:**
  - `{Function} callback`

- **Usage:** Call specified callback after a transition

---

### `disable()`

- **Usage:** Disables transitions. The instance will make immediate jumps to indexes instead of smooth movements

---

### `enable()`

- **Usage:** Enables previously disabled transitions