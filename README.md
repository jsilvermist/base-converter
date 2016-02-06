# base-converter

An element to use with data binding for converting or checking the base of a number.

Convert any number up to 2^53 (9,007,199,254,740,991),
to or from any base from base 2 to base 36.

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


## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

```sh
npm install -g bower
```

Then, go ahead and download the element's dependencies:

```sh
bower install
```


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
