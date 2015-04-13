# css-sprite-sass

[![NPM version](https://badge.fury.io/js/css-sprite-sass.svg)](http://badge.fury.io/js/css-sprite-sass) [![Build Status](https://travis-ci.org/aslansky/css-sprite-sass.svg?branch=master)](https://travis-ci.org/aslansky/css-sprite-sass) [![Dependencies](https://david-dm.org/aslansky/css-sprite-sass.svg)](https://david-dm.org/aslansky/css-sprite-sass)

> A sass/scss style processor for [css-sprite](https://npmjs.org/package/css-sprite)

## Requirements

- [css-sprite](https://npmjs.org/package/css-sprite) version >= 1.0

## Install

Install with [npm](https://npmjs.org/package/css-sprite-sass)

```
npm install css-sprite css-sprite-sass --save
```

If you want to use `css-sprite-sass` with the command line interface of `css-sprite` install it globally.

```
npm install css-sprite css-sprite-sass -g
```

## Options

* **style-type:** Eighter scss or sass. Defaults to scss.

## Usage

On commandline:

```sh
css-sprite out/ src/*.png -s style.scss -p css-sprite-sass --style-type scss
```

In JavaScript:

```js
var sprite = require('css-sprite');
sprite.create({
  ...
  style: 'style.scss',
  processor: 'css-sprite-sass'
  'style-type': 'scss'
  ...
}, function () {
  console.log('done');
});
```

#### [scss](http://sass-lang.com/) usage example

```scss
@import 'sprite'; // the generated style file (sprite.scss)

// camera icon (camera.png in src directory)
.icon-camera {
  @include sprite($camera);
}

// cart icon (cart.png in src directory)
.icon-cart {
  @include sprite($cart);
}
```

#### [sass](http://sass-lang.com/) usage example

```sass
@import 'sprite' // the generated style file (sprite.sass)

// camera icon (camera.png in src directory)
.icon-camera
  +sprite($camera)

// cart icon (cart.png in src directory)
.icon-cart
  +sprite($cart)
```

## More

See [css-sprite](https://npmjs.org/package/css-sprite) documentation
