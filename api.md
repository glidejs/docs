---
title: API
layout: docs.html
slug: api
priority: 5
algolia: true
---

[[lead]]Bunch of helpful properties and methods are available through Glide instance[[/lead]]

## Properties

### `index` <small>type: `{Number}`</small>

- **Usage:** Holds currently active zero-based slide index.

```js
var glide = new Glide('.glide', { startAt: 1 }).mount()

var i = glide.index // => 1
```

---

### `settings` <small>type: `{Object}`</small>

- **Usage:** Holds instance initialization settings.

```js
var glide = new Glide('.glide', { startAt: 1 }).mount()

var startAt = glide.settings.startAt // => 1
```

---

### `type` <small>type: `{String}`</small>

- **Usage:** Holds type of the Glide instance.

```js
var glide = new Glide('.glide').mount()

var type = glide.type // => 'slider'
```

---

### `disabled` <small>type: `{Boolean}`</small>

- **Usage:** Holds state of the ability to interact.

```js
var glide = new Glide('.glide').mount()

console.log(glide.disabled) // => false

glide.disable()

console.log(glide.disabled) // => true
```

---

## Methods

### `mount()`

- **Usage:** A Glide instance is in "uninitialized" mode until a `mount()` method call. It starts an entire building process.

```js
var glide = new Glide('.glide')

glide.mount()
```
- **Example:**

[[example dir=api/mount]]

---

### `update(settings)`

- **Arguments:**
  - `{Object} settings`

- **Usage:** Update settings for the Glide instance.

```js
var glide = new Glide('.glide', { startAt: 0 }).mount()

glide.update({ startAt: 1 })
```

- **Example:**

[[example dir=api/update]]

---

### `destroy()`

- **Usage:** Destroy instance and undo all modifications which have been made to the DOM. It also unbinds added event listeners.

```js
var glide = new Glide('.glide', { startAt: 0 }).mount()

glide.destroy()
```

- **Example:**

[[example dir=api/destroy]]

---

### `on(event, [definition])`

- **Arguments:**
  - `{String|Array} event`
  - `{Function} [definition]`

- **Usage:** Register callback which will be called at the specified events.

```js
var glide = new Glide('.glide')

glide.on('mount.after', function () {
  // Logic fired after mounting
})

glide.mount()
```

- **Example:**

[[example dir=api/on]]

---

### `go(pattern)`

- **Arguments:**
  - `{String} pattern`

- **Usage:** Make movement based on the defined pattern. A pattern must be in the special format:
  - `>` - Move one forward
  - `<` - Move one backward
  - `={i}` - Go to {i} zero-based slide (eq. '=1', will go to second slide)
  - `>>` - Rewinds to end (last slide)
  - `<<` - Rewinds to start (first slide)

```js
var glide = new Glide('.glide').mount()

glide.go('>')
```

- **Example:**

[[example dir=api/go]]

---

### `pause()`

- **Usage:** Stop auto-playing. Hold changing slides after a defined interval.

```js
var glide = new Glide('.glide', { autoplay: 4000 }).mount()

glide.pause()
```

- **Example:**

[[example dir=api/pause]]

---

### `play(force)`

- **Arguments:**
  - `{Number} force` Force to run auto-playing with passed interval regardless of `autoplay` settings

- **Usage:** Start previously stopped auto-playing.

```js
var glide = new Glide('.glide', { autoplay: 4000 }).mount()

glide.pause() // Pausing so we can resume it later

glide.play()
```

If instance was initialized with disabled autoplay, you can forcefully start it by passing interval number into `play()` method.

```js
var glide = new Glide('.glide', { autoplay: false }).mount()

glide.play(4000)
```

- **Example:**

[[example dir=api/play]]

---

### `disable()`

- **Usage:** Disable instance interaction. Blocks ability to manually change slides via controls or API.

```js
var glide = new Glide('.glide').mount()

glide.disable()
```

- **Example:**

[[example dir=api/disable]]

---

### `enable()`

- **Usage:** Enable previously disabled instance. Start responding to interaction.

```js
var glide = new Glide('.glide').mount()

glide.enable()
```

- **Example:**

[[example dir=api/enable]]

---

### `isType(type)`

- **Arguments:**
  - `{String} type`

- **Usage:** Verify the type of a Glide instance.

```js
var slider = new Glide('.glide', { type: 'carousel' }).mount()

slider.isType('slider') // => false
slider.isType('carousel') // => true
```