---
title: Clones
layout: docs.html
slug: clones
algolia: true
---

[[lead]]Manages creating and deleting clone HTML elements of slides for looping of carousel type[[/lead]]

## Usage <small>type: `required`</small>

This module is requisite and it's imported within a bundle.

## Properties

### `items` <small>type: `{HTMLCollection}`</small>

- **Usage:** Holds collection HTML elements of the cloned slides

---

### `pattern` <small>type: `{Array}`</small>

- **Usage:** Holds slides indexes pattern for cloning

---

### `grow` <small>type: `{Number}`</small>

- **Usage:** Holds additional dimentions value caused by clone HTML elements

## Methods

### `mount()`

- **Usage:** Mounts and initializes a component

---

### `map(pattern)`

- **Arguments:**
  - `{Array} pattern`

- **Returns:** Array

- **Usage:** Generates slides indexes pattern for cloning

---

### `collect(items)`

- **Arguments:**
  - `{HTMLCollection} items`

- **Returns:** HTMLCollection

- **Usage:** Creates a collection of cloned slides using indexes pattern

---

### `append()`

- **Usage:** Appends collection of clones into DOM using indexes pattern

---

### `remove()`

- **Usage:** Removes  HTML elements of clones from the DOM