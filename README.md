# EQuery.js 3.0.4

EQuery.js is a lightweight, versatile DOM manipulation and event management utility library. It provides a jQuery-like syntax for selecting elements, handling events, and performing common UI tasks such as dragging, resizing, and image magnification.

## Table of Contents

* [Installation](#installation)
* [Basic Usage](#basic-usage)
* [Core Features](#core-features)
* [DOM Selection & Manipulation](#dom-selection--manipulation)
* [Event Handling](#wvent-handling)
* [UI Utilities](#ui-utilities)
* [Canvas & Storage Helpers](#canvas--storage-helpers)


* [API Reference](#api-reference)

---

## Installation

EQuery supports multiple module formats including CommonJS, AMD, and direct browser script inclusion.

```html
<script src="path/to/equery.js"></script>
<script>
  const $ = EQuery;
</script>

```

---

## Basic Usage

The library uses the `q` or `EQuery` function as a selector factory. It returns an EQuery collection wrapping the DOM nodes.

```javascript
// Select elements and change style
EQuery('.my-class').css('color: red');

// Create a new element and append it
EQuery.elemt('div', 'Hello World', 'my-new-div').append('body');

// Handle click events
EQuery('#my-button').on('click', function() {
    console.log('Button clicked!');
});

```

---

## Core Features

### DOM Selection & Manipulation

EQuery allows for efficient querying and manipulation of DOM elements.

* **Selection**: Supports CSS selectors, DOM elements, or arrays of elements.
* **Styling**: Use `.css()` to apply inline styles or `.addClass()`/`.removeClass()` for class management.
* **Content**: Modify HTML content with `.html()`, `.text()`, `.append()` and `.val()`.

### Event Handling

The library provides a robust event system that handles cross-browser inconsistencies and supports passive events.

* **Standard Events**: `.on()`, `.off()`, and `.trigger()`.
* **One-time Events**: `.one()` and `.any()` for handlers that execute only once.
* **Event Map**: Includes shorthand methods for common events like `.click()`, `.hover()`, `.keydown()`, and touch events.

### UI Utilities

EQuery includes several built-in UI enhancements:

* **Drag & Resize**: Make any element draggable using `.dragElement()` or resizable with `.resize()`.
* **Image Magnification**: Add a magnifying glass effect to images using `.magnify(zoomLevel)`.
* **Spinners**: Easily create and append loading indicators with `.spinner()`.
* **Alerts/Comments**: Display temporary notifications using `.newComment(text, type)`.

### Canvas & Storage Helpers

* **Canvas Wrapper**: High-level API for drawing circles, lines, and boxes on a canvas element.
* **IndexedDB Storage**: A structured storage helper for persisting application state using IndexedDB.

---

## API Reference

### Global Utility Functions

| Method | Description |
| --- | --- |
| `EQuery.elemt(tag, content, class, attrs, style)` | Creates and wraps a new DOM element. |
| `EQuery.ajax(options)` | Performs asynchronous HTTP requests. |
| `EQuery.createLogger(name)` | Creates a namespaced logger with history and levels (debug, info, warn, error). |
| `EQuery.setCookie(name, value, days)` | Utility for managing browser cookies. |

### Instance Methods (on EQuery collections)

| Method | Description |
| --- | --- |
| `.each(callback)` | Iterates over every element in the collection. |
| `.find(selector)` | Searches for descendants matching the selector. |
| `.hide()` / `.show()` | Toggles visibility by setting `display: none` or `display: block`. |
| `.append(content)` | Appends content (string or element) to the selected elements. |
| `.attr(key, value)` | Gets or sets attributes on elements. |

---

## License

EQuery.js is licensed under Sharon Abodunrin.
