---
title: Events
layout: docs.html
slug: events
priority: 4
algolia: true
---

[[lead]]Glide.js comes with a rich collection of events that you can listen in order to run a custom logic at specific moments[[/lead]]

Use `.on(event, handler)` method to assign your custom listeners.

> Remember to declare your event listeners before calling `mount()` method.

```js
var glide = new Glide('.glide')

glide.on('mount.before', function() {
  // Handler logic ...
})

glide.mount()
```

You can also bind a single handler to multiple events using an array of names.

```js
glide.on(['mount.before', 'run'], function() {
  // Handler logic ...
})
```

## Reference

### `mount.before`

Called before first mounting begins. However, the mounting phase has not been started, and components are not bootstrapped yet.

---

### `mount.after`

Called right after first mounting. All components have been mounted.

---

### `update`

Called right after updating settings with `update()` API method.

---

### `play`

Called right after starting an instance with `play()` API method.

---

### `pause`

Called right after stopping instance with `pause()` API method.

---

### `build.before`

Called right before setting up a slider to its initial state. At this point, classes, translations, and sizes are applied.

---

### `build.after`

Called right after setting up a slider to its initial state. At this point, classes, translations, and sizes are applied.

---

### `run.before`

**Arguments:**
- `{Object} move`

Called right before calculating new index and making a transition. The movement schema (eg. `=1`) string has been parsed.

---

### `run`

**Arguments:**
- `{Object} move`

Called right after calculating new index and before making a transition. The movement schema (eg. `=1`) string has been parsed.

---

### `run.after`

**Arguments:**
- `{Object} move`

Called after calculating new index and making a transition. The movement schema (eg. `=1`) string has been parsed.

---

### `run.offset`

**Arguments:**
- `{Object} move`

Called after calculating new index and making a transition, while we did an offset animation. Offset animation take place at two moments:
- changing slide from first to the last one
- changing slide from last to the first one

---

### `run.start`

**Arguments:**
- `{Object} move`

Called right after calculating the new index, but before making a transition, while we did a rewinding to the start index.

---

### `run.end`

**Arguments:**
- `{Object} move`

Called right after calculating the new index, but before making a transition, while we did a rewinding to the last index.

---

### `move`

**Arguments:**
- `{Number} movement`

Called right before movement transition begins.

---

### `move.after`

**Arguments:**
- `{Number} movement`

Called right after movement transition ends.

---

### `resize`

Called when the window is being resized. This event throttled

---

### `swipe.start`

Called right after swiping begins.

---

### `swipe.move`

Called during swiping movement.

---

### `swipe.end`

Called right after swiping ends.

---

### `translate.jump`

**Arguments:**
- `{Number} movement`

Called right before a translate applies, while we doing a jump to the first or last slide from offset movement. This event is only used when a type is set up to `carousel`.

---
