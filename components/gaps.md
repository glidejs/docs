---
title: Gaps
layout: docs.html
slug: gaps
algolia: true
---

[[lead]]Responsible for applying gaps between slides[[/lead]]

## Usage <small>type: `required`</small>

This module is requisite and it's imported within a bundle.

## Properties

### `value` <small>type: `{Number}`</small>

- **Usage:** Holds value of gaps

---

### `grow` <small>type: `{Number}`</small>

- **Usage:** Holds additional dimensions value caused by gaps. Used to increase the width of the slides wrapper

---

### `reductor` <small>type: `{Number}`</small>

- **Usage:** Holds reduction value caused by gaps. Used to subtract the width of the slides

## Methods

### `mount()`

- **Usage:** Mounts and initializes a component

---

### `apply(slides)`

- **Arguments:**
  - `{HTMLCollection} slides`

- **Usage:** Applies gaps between slides. First and last slides do not receive it's edge margins

---

### `remove(slides)`

- **Arguments:**
  - `{HTMLCollection} slides`

- **Usage:** Removes gaps from the slides.
