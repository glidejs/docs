---
title: Options
layout: docs.html
slug: options
priority: 6
algolia: true
---

[[lead]]Glide can be adjusted with various options. Pass an object as an argument while initializing a new instance[[/lead]]

```js
new Glide('.glide', {
  type: 'carousel',
  startAt: 0,
  perView: 3
})
```

## Reference

### `type` <small>default: `'slider'` type: `String`</small>

Type of the movement. Available types:
- `slider` - rewinds slider to the start/end when it reaches first or last slide,
- `carousel` - changes slides without starting over when it reaches first or last slide.

[[example dir=options/type]]

---

### `startAt` <small>default: `0` type: `Number`</small>

Start at specific slide number defined with zero-based index.

[[example dir=options/start-at]]

---

### `perView` <small>default: `1` type: `Number`</small>

A number of slides visible on the single viewport.

[[example dir=options/per-view]]

---

### `focusAt` <small>default: `0` type: `Number|String`</small>

Focus currently active slide at a specified position in the track. Available inputs:
- `'center'` - current slide will be always focused at the center of a track,
- `1,2,3...` - current slide will be focused on the specified zero-based index.

[[example dir=options/focus-at]]

---

### `gap` <small>default: `10` type: `Number`</small>

A size of the gap added between slides.

[[example dir=options/gap]]

---

### `autoplay` <small>default: `false` type: `Number|Boolean`</small>

Change slides after a specified interval. Use `false` for turning off autoplay.

[[example dir=options/autoplay]]

---

### `hoverpause` <small>default: `true` type: `Boolean`</small>

Stop autoplay on mouseover event.

[[example dir=options/hoverpause]]

---

### `keyboard` <small>default: `true` type: `Boolean`</small>

Allow for changing slides with left and right keyboard arrows.

[[example dir=options/keyboard]]

---

### `swipeThreshold` <small>default: `80` type: `Number|Boolean`</small>

Minimal swipe distance needed to change the slide. Use `false` for turning off a swiping.

[[example dir=options/swipe-threshold]]

---

### `dragThreshold` <small>default: `120` type: `Number|Boolean`</small>

Minimal mouse drag distance needed to change the slide. Use `false` for turning off a dragging.

[[example dir=options/drag-threshold]]

---

### `perTouch` <small>default: `false` type: `Number|Boolean`</small>

A maximum number of slides to which movement will be made on swiping or dragging. Use `false` for unlimited.

[[example dir=options/per-touch]]

---

### `touchRatio` <small>default: `0.5` type: `Number`</small>

Alternate moving distance ratio of the slides on a swiping and dragging.

[[example dir=options/touch-ratio]]

---

### `touchAngle` <small>default: `45` type: `Number`</small>

Angle required to activate slides moving on swiping or dragging.

[[example dir=options/touch-angle]]

---

### `animationDuration` <small>default: `400` type: `Number`</small>

Duration of the animation in milliseconds.

[[example dir=options/animation-duration]]

---

### `rewind` <small>default: `true` type: `Boolean`</small>

Allows looping the `slider` type. Slider will rewind to the first/last slide when it's at the start/end.

---

### `rewindDuration` <small>default: `800` type: `Number`</small>

Duration of the rewinding animation of the `slider` type in milliseconds.

[[example dir=options/rewind-duration]]

---

### `animationTimingFunc` <small>default: `'cubic-bezier(0.165, 0.840, 0.440, 1.000)'` type: `String`</small>

Easing function for the animation.

[[example dir=options/animation-timing-func]]

---

### `direction` <small>default: `'ltr'` type: `String`</small>

Moving direction mode. Available inputs:
- 'ltr' - left to right movement,
- 'rtl' - right to left movement.

[[example dir=options/direction]]

---

### `peek` <small>default: `0` type: `Number|Object`</small>

The distance value of the next and previous viewports which have to peek in the current view. Accepts number and pixels as a string. Left and right peeking can be setup separately with a directions object. For example:
- `100` - peek 100px on the both sides,
- `{ before: 100, after: 50 }` - peek 100px on the left side and 50px on the right side.

[[example dir=options/peek]]

---

### `breakpoints` <small>default: `{}` type: `Object`</small>

Collection of options applied at specified media breakpoints. For example, display two slides per view under 800px:
```
{
  800: {
    perView: 2
  }
}
```

[[example dir=options/breakpoints]]

---

### `classes` <small>type: `Object`</small>

Collection of internally used HTML classes. Default values:

```
{
  direction: {
    ltr: 'glide--ltr',
    rtl: 'glide--rtl'
  },
  slider: 'glide--slider',
  carousel: 'glide--carousel',
  swipeable: 'glide--swipeable',
  dragging: 'glide--dragging',
  cloneSlide: 'glide__slide--clone',
  activeNav: 'glide__bullet--active',
  activeSlide: 'glide__slide--active',
  disabledArrow: 'glide__arrow--disabled'
}
```

---

### `throttle` <small>default: `25` type: `Number`</small>

Throttle costly events at most once per every wait milliseconds.
