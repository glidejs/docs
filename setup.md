---
title: Setup
layout: docs.html
slug: setup
priority: 7
algolia: true
---

### Installation

There are several ways to pull-in Glide.js into your project.

#### NPM

It is a recommended way. This installation method guarantees a trouble-free use with bundlers like [Webpack](//webpack.js.org/) or [Rollup](//rollupjs.org/).

```bash
# Install the last stable version
$ npm install @glidejs/glide
```

#### Download

You can also traditionally download latest files from the Github:

<a class="button" href="//github.com/glidejs/glide/releases/latest">Download latest release</a>

#### CDN

You can also use a reference to some of the popular CDN services:
- [https://cdn.jsdelivr.net/npm/@glidejs/glide](https://cdn.jsdelivr.net/npm/@glidejs/glide)
- [https://unpkg.com/@glidejs/glide](https://unpkg.com/@glidejs/glide)

### Explanation of Different Builds

Glide.js is built in a few different variants. They can be found in the `dist/` directory.

- **Complete** - Builds that contains both required and optional modules.
- **Modular** - Builds that contains only required modules. Optional modules are exported for import on demand.

|   | UMD | ES Module |
|---|---|---|
| Complete | glide.js  | glide.esm.js |
| Modular | --- | glide.modular.esm.js |
| Complete (minified) | glide.min.js | --- |

## Configuration

[[lead]]It is required to prepare necessary markup and essential styles[[/lead]]

### Styling

Glide.js styles are divided into two separate files:
- `glide.core` - Core styles, required for Glide.js to work
- `glide.theme` - Visual styles. Optional styling for markup.

This way, the library doesn't force you to overwrite it's visual styles if you want to implement your own look.

#### Using `<link>`

Provide `<link>` to the stylesheets `.css` files.

```html
<!-- Required Core Stylesheet -->
<link rel="stylesheet" href="node_modules/@glidejs/glide/dist/css/glide.core.min.css">

<!-- Optional Theme Stylesheet -->
<link rel="stylesheet" href="node_modules/@glidejs/glide/dist/css/glide.theme.min.css">
```

#### Using SASS `@import`

Import `.scss` files directly from the source directory.

```scss
// Required Core Stylesheet
@import "node_modules/@glidejs/glide/src/assets/sass/glide.core";

// Optional Theme Stylesheet
@import "node_modules/@glidejs/glide/src/assets/sass/glide.theme";
```

### Structure

Prepare the main markup. Remember to add a `data-glide-el="track"` attribute on track element.

```html
<div class="glide">
  <div class="glide__track" data-glide-el="track">
    <ul class="glide__slides">
      <li class="glide__slide">0</li>
      <li class="glide__slide">1</li>
      <li class="glide__slide">2</li>
    </ul>
  </div>
</div>
```

### Controls

Creating controls involves using two data attributes:
- `data-glide-el="controls"` - Controls wrapper indicator that contains all controls elements
- `data-glide-dir="{pattern}"` - Movement schema of the particular control

```html
<div data-glide-el="controls">
  <button data-glide-dir="<<">Start</button>
  <button data-glide-dir=">>">End</button>
</div>
```

Schema value of the `data-glide-dir` attribute must be in special format:
- `>` - Move one forward
- `<` - Move one backward
- `={i}` - Go to zero-based {i} slide (eq. '=1', will go to second slide)
- `>>` - Rewinds to the end (last slide)
- `<<` - Rewinds to the start (first slide)

#### Arrows

Knowing about the controls, preparing the arrows navigation is quite simple.

```html
<div class="glide">
  <div class="glide__track" data-glide-el="track">...</div>

  <div class="glide__arrows" data-glide-el="controls">
    <button class="glide__arrow glide__arrow--prev" data-glide-dir="<">prev</button>
    <button class="glide__arrow glide__arrow--next" data-glide-dir=">">next</button>
  </div>
</div>
```

#### Bullets

Making a bullets navigation is pretty similar. However, use the `data-glide-el="controls[nav]"` to activate toggling an activity class on control elements inside.

```html
<div class="glide">
  <div class="glide__track" data-glide-el="track">...</div>

  <div class="glide__bullets" data-glide-el="controls[nav]">
    <button class="glide__bullet" data-glide-dir="=0"></button>
    <button class="glide__bullet" data-glide-dir="=1"></button>
    <button class="glide__bullet" data-glide-dir="=2"></button>
  </div>
</div>
```

## Initialization

[[lead]]Finally, we are ready to initialize and mount a Glide[[/lead]]

#### Using `<script>`

Simply reference a minified version of the script.

```html
<script src="node_modules/@glidejs/glide/dist/glide.min.js"></script>

<script>
  new Glide('.glide').mount()
</script>
```

#### Using ES Modules

```js
import Glide from '@glidejs/glide'

new Glide('.glide').mount()
```

Need a few selected modules? Import and mount only needed components. In pair with a bundler's [tree-shaking](//webpack.js.org/guides/tree-shaking/) it's a great way to reduce the total weight your code!

> Notice that we are using here a path to the modular build. Go back to [explanation]() section to learn more.

```js
import Glide, { Controls, Breakpoints } from '@glidejs/glide/dist/glide.modular.esm'

new Glide('.glide').mount({ Controls, Breakpoints })
```
