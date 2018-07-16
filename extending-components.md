---
title: Extending Components
layout: docs.html
slug: extending-components
priority: 1
algolia: true
---

[[lead]]Glide is structured with components. They encapsulate specific functionalities into single modules[[/lead]]

## Using Components

The component is a simple `function` that returns an `object`. Each component has a single responsibility and communicates with other components using events.

#### Creating Custom Components

Inside component constructor you have access to three arguments that are passed on initialization:
- `{Glide} Glide` - A current instance of the Glide class,
- `{Object} Components` - A collection of all registered components,
- `{EventsBus} Events` - A instance of EventsBus class for events interaction.

A constructor should return an object. If it contains a `mount()` method it will be called automatically on Glide instance mounting.

```js
/**
 * An example component to extend Glide functionalities.
 *
 * @param {Glide} Glide
 * @param {Object} Components
 * @param {EventsBus} Events
 */
var Example = function (Glide, Components, Events) {
  return {
    mount () {
      console.log('Example component has been mounted.')
    }
  }
}
```

#### Registering Components

In order to register created component, pass a collection of components to `mount()` method at Glide initialization.

> Important! Keyword under which component is registered should be unique, otherwise will overwrite existing component.

```js
var Example = function (Glide, Components, Events) {
  return {
    mount () {
      //
    }
  }
}

new Glide('.glide').mount({
  'Example': Example
})
```

#### Accessing Components

After registration, a component can be accessed thru the `Components` object which contains the collection of all added components.

```js
function (Glide, Components, Events) {
  var example = Components.Example
}
```

#### Listening for Events

Inside component's function, you have a direct access to the EventsBus instance. That allows you to easily create component-specific event listeners.

```js
function (Glide, Components, Events) {
  var Example = {
    mount () {
      Events.emit('example.mount')
    },

    method () {
      console.log('This method has been called on `mount.after` event.')
    }
  }

  Events.on('mount.after', function () {
    Example.method()
  })

  return Example
}
```