---
title: Extending Transformers
layout: docs.html
slug: extending-transformers
priority: 2
algolia: true
---

[[lead]]Glide uses transformers to mutate `translate` value. They mutates it's value to achieve e.q. centered focusing or right-to-left movement.[[/lead]]

## Using Transformers

The transformer is a simple `function` that returns an `object` with `modify()` method.

> It's importand to understand that transformers works like piplines - previously modified value is passed to the next transformer, so order of transformers matters!

#### Creating Custom Transformers

Inside component constructor you have access to three arguments that are passed on initialization:
- `{Glide} Glide` - A current instance of the Glide class,
- `{Object} Components` - A collection of all registered components,
- `{EventsBus} Events` - A instance of EventsBus class for events interaction.

A constructor should return an object. It have to contains a `modify()` method which receives current translate value as a argument. The `modify()` method should always return a `Number`.

```js
/**
 * Update translate value by 100.
 *
 * @param  {Glide} Glide
 * @param  {Object} Components
 * @param  {EventsBus} Events
 * @return {Object}
 */
var Example = function (Glide, Components, Events) {
  return {
    /**
     * Modifies passed translate value by 100 pixels.
     *
     * @param  {Number} translate
     * @return {Number}
     */
    modify (translate) {
      return translate + 100
    }
  }
}
```

#### Registering Transformers

In order to register created transformer, pass an array of transformers to `mutate()` method at Glide initialization.

> Important! Transformers should be registered before `mount()` call.

```js
var Example = function (Glide, Components, Events) {
  return {
    modify (translate) {
      //
    }
  }
}

new Glide('.glide')
  .mutate([Example])
  .mount()
```