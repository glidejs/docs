---
title: Run
layout: docs.html
slug: run
algolia: true
---

[[lead]]Responsible for calculating a currently active index based on movement[[/lead]]

## Usage <small>type: `required`</small>

This module is requisite and it's imported within a bundle.

## Properties

### `move` <small>type: `{Object}`</small>

- **Usage:** Holds value of the current movement. For example, `=1` schema will be represented as:

```js
{
  direction: '=',
  steps: '1'
}
```

---

### `length` <small>type: `{Number}`</small>

- **Usage:** Holds a zero-based value of the running distance

---

### `offset` <small>type: `{Boolean}`</small>

- **Usage:** Holds an indication flag about making rewinding movement

## Methods

### `mount()`

- **Usage:** Mounts and initializes a component

---

### `make(move)`

- **Arguments:**
  - `{String} move`

- **Usage:** Makes instance run based on the passed moving schema

---

### `calculate()`

- **Usage:** Calculates current index based on the defined move

---

### `isStart()`

- **Usage:** Checks if we currently are on the first slide

---

### `isEnd()`

- **Usage:** Checks if we currently are on the last slide

---

### `isOffset(direction)`

- **Arguments:**
  - `{String} direction`

- **Usage:** Checks if we are making an offset run, from last to first or first to last slide
