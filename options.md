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

- [`type`](#type) - Type of the movement
- [`startAt`](#startat) - Start at specific slide number
- [`perView`](#perview) - A number of visible slides
- [`focusAt`](#focusat) - Focus currently active slide at a specified position
- [`gap`](#gap) - A size of the space between slides
- [`autoplay`](#autoplay) - Change slides after a specified interval
- [`hoverpause`](#hoverpause) - Stop autoplay on mouseover
- [`keyboard`](#keyboard) - Change slides with keyboard arrows
- [`bound`](#bound) - Stop running `perView` number of slides from the end
- [`swipeThreshold`](#swipethreshold) - Minimal swipe distance needed to change the slide
- [`dragThreshold`](#dragthreshold) - Minimal mousedrag distance needed to change the slide
- [`perTouch`](#pertouch) - A maximum number of slides moved per single swipe or drag
- [`touchRatio`](#touchratio) - Alternate moving distance ratio of swiping and dragging
- [`touchAngle`](#touchangle) - Angle required to activate slides moving
- [`animationDuration`](#animationduration) - Duration of the animation
- [`rewind`](#rewind) - Allow looping the `slider` type
- [`rewindDuration`](#rewindduration) - Duration of the rewinding animation
- [`animationTimingFunc`](#animationtimingfunc) - Easing function for the animation
- [`direction`](#direction) - Moving direction mode
- [`peek`](#peek) - The value of the future viewports which have to be visible in the current view
- [`breakpoints`](#breakpoints) - Collection of options applied at specified media breakpoints
- [`classes`](#classes) - Collection of used HTML classes
- [`throttle`](#throttle) - Throttle costly events

---

### `type`

Type of the movement. Available types:
- `slider` - rewinds slider to the start/end when it reaches first or last slide,
- `carousel` - changes slides without starting over when it reaches first or last slide.

<small>default: `'slider'` type: `String`</small>

[[example dir=options/type]]

---

### `startAt`

Start at specific slide number defined with zero-based index.

<small>default: `0` type: `Number`</small>

[[example dir=options/start-at]]

---

### `perView`

The number of slides visible on the single viewport.

<small>default: `1` type: `Number`</small>

[[example dir=options/per-view]]

---

### `focusAt`

Focus currently active slide at a specified position in the track. Available inputs:
- `'center'` - current slide will be always focused at the center of a track,
- `1,2,3...` - current slide will be focused on the specified zero-based index.

<small>default: `0` type: `Number|String`</small>

[[example dir=options/focus-at]]

---

### `gap`

The size of the gap added between slides.

<small>default: `10` type: `Number`</small>

[[example dir=options/gap]]

---

### `autoplay`

Change slides after a specified interval. Use `false` for turning off autoplay.

<small>default: `false` type: `Number|Boolean`</small>

[[example dir=options/autoplay]]

---

### `hoverpause`

Stop autoplay on mouseover event.

<small>default: `true` type: `Boolean`</small>

[[example dir=options/hoverpause]]

---

### `keyboard`

Allow for changing slides with left and right keyboard arrows.

<small>default: `true` type: `Boolean`</small>

[[example dir=options/keyboard]]

---

### `bound`

> Works only with `slider` type and a non-centered `focusAt` setting.

Stop running `perView` number of slides from the end. Use this option if you don't want to have an empty space after a slider.

<small>default: `false` type: `Boolean`</small>

[[example dir=options/bound]]

---

### `swipeThreshold`

Minimal swipe distance needed to change the slide. Use `false` for turning off swiping.

<small>default: `80` type: `Number|Boolean`</small>

[[example dir=options/swipe-threshold]]

---

### `dragThreshold`

Minimal mouse drag distance needed to change the slide. Use `false` for turning off a dragging.

<small>default: `120` type: `Number|Boolean`</small>

[[example dir=options/drag-threshold]]

---

### `perTouch`

A maximum number of slides to which movement will be made on swiping or dragging. Use `false` for unlimited.

<small>default: `false` type: `Number|Boolean`</small>

[[example dir=options/per-touch]]

---

### `touchRatio`

Alternate moving distance ratio of the slides on swiping and dragging.

<small>default: `0.5` type: `Number`</small>

[[example dir=options/touch-ratio]]

---

### `touchAngle`

Angle required to activate slides moving on swiping or dragging.

<small>default: `45` type: `Number`</small>

[[example dir=options/touch-angle]]

---

### `animationDuration`

Duration of the animation in milliseconds.

<small>default: `400` type: `Number`</small>

[[example dir=options/animation-duration]]

---

### `rewind`

> Works only with `slider` type.

Allows looping the `slider` type. Slider will rewind to the first/last slide when it's at the start/end.

<small>default: `true` type: `Boolean`</small>

[[example dir=options/rewind]]

---

### `rewindDuration`

Duration of the rewinding animation of the `slider` type in milliseconds.

<small>default: `800` type: `Number`</small>

[[example dir=options/rewind-duration]]

---

### `animationTimingFunc`

Easing function for the animation.

<small>default: `'cubic-bezier(0.165, 0.840, 0.440, 1.000)'` type: `String`</small>

[[example dir=options/animation-timing-func]]

---

### `direction`

Moving direction mode. Available inputs:
- 'ltr' - left to right movement,
- 'rtl' - right to left movement.

<small>default: `'ltr'` type: `String`</small>

[[example dir=options/direction]]

---

### `peek`

The distance value of the next and previous viewports which have to peek in the current view. Accepts number and pixels as a string. Left and right peeking can be set up separately with a directions object. For example:
- `100` - peek 100px on the both sides,
- `{ before: 100, after: 50 }` - peek 100px on the left side and 50px on the right side.

<small>default: `0` type: `Number|Object`</small>

[[example dir=options/peek]]

---

### `breakpoints`

Collection of options applied at specified media breakpoints. For example, display two slides per view under 800px:
```
{
  800: {
    perView: 2
  }
}
```

<small>default: `{}` type: `Object`</small>

[[example dir=options/breakpoints]]

---

### `classes`

Collection of internally used HTML classes. Default values:

<small>type: `Object`</small>

```
{
  swipeable: 'glide--swipeable',
  dragging: 'glide--dragging',
  direction: {
    ltr: 'glide--ltr',
    rtl: 'glide--rtl'
  },
  type: {
    slider: 'glide--slider',
    carousel: 'glide--carousel'
  },
  slide: {
    clone: 'glide__slide--clone',
    active: 'glide__slide--active'
  },
  arrow: {
    disabled: 'glide__arrow--disabled'
  },
  nav: {
    active: 'glide__bullet--active'
  }
}
```

---

### `throttle`

Throttle costly events at most once per every wait milliseconds.

<small>default: `25` type: `Number`</small>
