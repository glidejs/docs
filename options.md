---
title: Options
layout: docs.html
slug: options
priority: 6
algolia: true
---

- [Reference](#reference)
  - [`type`](#type)
  - [`startAt`](#startAt)
  - [`perView`](#perView)
  - [`focusAt`](#focusAt)
  - [`gap`](#gap)
  - [`autoplay`](#autoplay)
  - [`hoverpause`](#hoverpause)
  - [`keyboard`](#keyboard)
  - [`bound`](#bound)
  - [`swipeThreshold`](#swipeThreshold)
  - [`dragThreshold`](#dragThreshold)
  - [`perTouch`](#perTouch)
  - [`touchRatio`](#touchRatio)
  - [`touchAngle`](#touchAngle)
  - [`animationDuration`](#animationDuration)
  - [`rewind`](#rewind)
  - [`rewindDuration`](#rewindDuration)
  - [`animationTimingFunc`](#animationTimingFunc)
  - [`direction`](#direction)
  - [`peek`](#peek)
  - [`breakpoints`](#breakpoints)
  - [`classes`](#classes)
  - [`throttle`](#throttle)

[[lead]]Glide can be adjusted with various options. Pass an object as an argument while initializing a new instance[[/lead]]

```js
new Glide('.glide', {
  type: 'carousel',
  startAt: 0,
  perView: 3
})
```

## Reference

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

A number of slides visible on the single viewport.

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

A size of the gap added between slides.

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

Minimal swipe distance needed to change the slide. Use `false` for turning off a swiping.

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

Alternate moving distance ratio of the slides on a swiping and dragging.

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

The distance value of the next and previous viewports which have to peek in the current view. Accepts number and pixels as a string. Left and right peeking can be setup separately with a directions object. For example:
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

### `throttle`

Throttle costly events at most once per every wait milliseconds.

<small>default: `25` type: `Number`</small>
