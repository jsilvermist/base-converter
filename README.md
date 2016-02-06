# base-converter

An element to use with data binding for converting or checking the base of a number.

Convert any number up to 2^53 (9,007,199,254,740,991),
to or from any base from base 2 to base 36.

### Demo

For demos and documentation visit the [base-converter GitHub.io Page](http://jsilvermist.github.io/base-converter/components/base-converter/).

### Examples

Conversion Example:

```html
<template is="dom-bind">
  <base-converter number="ff" from="16" to="10" result="{{result}}"></base-converter>
  <p>Number: ff; From: 16; To: 10</p>
  <p>The result is: {{result}}</p>
</template>
```

Checking Example:

```html
<template is="dom-bind">
  <base-converter number="92" from="8" valid="{{isValid}}"></base-converter>
  <p>Number: 92; Base: 8</p>
  <p>The number is a valid base 8 number: {{isValid}}</p>
</template>
```

> Note: Conversion and checking can be used both together or separetely.

To use the values inside of JavaScript but outside of a Polymer element,
add an ID to your template and select it, then access the data-bindings.

```html
<template is="dom-bind" id="app">
  <base-converter number="255" from="10" to="16" result="{{converted}}">
  </base-converter>
</template>

<script>
  document.addEventListener('WebComponentsReady', function() {
    var app = document.querySelector('#app');
    console.log('JavaScript: The result is ' + app.converted);
  });
</script>
```


## How To Use

### Installation

The best way to install this element is through [Bower](http://bower.io/).

If you don't already have bower installed, install [Node.js](nodejs.org),
open a terminal window and type:

```sh
npm install -g bower
```

Once you have bower installed, you may want to use `bower init` to initialize your project.
This will enable you to save packages you install to make it easier to update,
and install all dependencies again later.

To install this element, type:

```sh
bower install --save base-converter
```

### Using

To use the element after installing it, first load webcomponents polyfill in the head of your page
(Recommended to be loaded at the top before any other scripts):

```html
<script src="bower_components/webcomponentsjs/webcomponents-lite.js"></script>
```

Second, import the element before using it (this can be in the head or wherever you wish):

```html
<link rel="import" href="bower_components/base-converter/base-converter.html">
```

Ensure that the path to bower_components is correct if it's not in the same directory.


## Playing With The Element

If you wish to work on the element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep the element's
bower dependencies in line. You can install it via:

```sh
npm install -g polyserve
```

And you can run it via:

```sh
polyserve
```

Once running, you can preview the element at
`http://localhost:8080/components/base-converter/`, where `base-converter` is the name of the directory containing it.

### Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install all of the element's dependencies via:

```sh
bower install
```
