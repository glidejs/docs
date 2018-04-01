---
title: Data Attributes
layout: docs.html
slug: data-attributes
priority: 3
algolia: true
---

[[lead]]There are few `data` attributes which additionally helps you to control and customize Glide instances from HTML level[[/lead]]

### `data-glide-el="track"`

Points a track element which includes slides markup.

```html
<div class="glide">
  <div class="glide__track" data-glide-el="track">...</div>
</div>
```

---

### `data-glide-el="controls"`

Points to an element that contains controls. Elements inside will have event bounded so they can guide movements on `click` event.

```html
<div class="glide">
  <div data-glide-el="controls">
    <button data-glide-dir="<<">start</button>
    <button data-glide-dir=">>">end</button>
  </div>
</div>
```

---

### `data-glide-el="controls[nav]"`

Special variant of standard `data-glide-el="controls"` attribute. Elements inside will have an active class toggled based on currently active slide index.

```html
<div class="glide">
  <div data-glide-el="controls[nav]">
    <button data-glide-dir="=0"></button>
    <button data-glide-dir="=1"></button>
    <button data-glide-dir="=2"></button>
  </div>
</glide>
```

---

### `data-glide-dir="{pattern}"`

Defines movement pattern of the specified control when it will be clicked. A pattern must be in the special format:
- `>` - Move one forward
- `<` - Move one backward
- `={i}` - Go to {i} zero-based slide (eq. '=1', will go to second slide)
- `>>` - Rewinds to end (last slide)
- `<<` - Rewinds to start (first slide)

```html
<div class="glide">
  <div data-glide-el="controls">
    <button data-glide-dir="<">prev</button>
    <button data-glide-dir=">">next</button>
  </div>
</div>
```

---

### `data-glide-autoplay="{number}"`

Allows for changing autoplay duration at the specified slide. Autoplay will be delayed at precise slide regardless of the `autoplay` option setup at initialization.

```html
<div class="glide">
  <div class="glide__track" data-glide-el="track">
    <ul class="glide__slides">
      <li class="glide__slide">0</li>
      <li class="glide__slide" data-glide-autoplay="6000">1</li>
      <li class="glide__slide">2</li>
    </ul>
  </div>
</div>
```

```js
new Glide('.glide', {
  autoplay: 4000
})
```
