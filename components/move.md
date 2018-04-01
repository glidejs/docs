---
title: Move
layout: docs.html
slug: move
algolia: true
---

[[lead]]Responsible for calculating a movement distance[[/lead]]

## Usage <small>type: `required`</small>

This module is requisite and it's imported within a bundle.

## Properties

### `value` <small>type: `{Number}`</small>

- **Usage:** Holds an actual movement value corrected by an offset

---

### `translate` <small>type: `{Number}`</small>

- **Usage:** Holds a raw movement value calculated based on the current index

---

### `offset` <small>type: `{Number}`</small>

- **Usage:** Holds an offset value used to modify current translate value

## Methods

### `mount()`

- **Usage:** Mounts and initializes a component

---

### `make(offset)`

- **Arguments:**
  - `{Number} offset`

- **Usage:** Calculates a movement value based on the passed offset and currently active index