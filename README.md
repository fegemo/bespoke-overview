[![Build Status](https://secure.travis-ci.org/fegemo/bespoke-overview.png?branch=master)](https://travis-ci.org/fegemo/bespoke-overview) [![Coverage Status](https://coveralls.io/repos/fegemo/bespoke-overview/badge.png)](https://coveralls.io/r/fegemo/bespoke-overview)

# bespoke-simple-overview

Displays an overview version of a bespoke presentation when `Esc` (configurable)
is pressed.

![Presentation with the overview mode off, showing one slide - the current one](docs/overview-mode-off.png)
![Presentation with the overview mode on, showing about 5 slides](docs/overview-mode-on.png)

## Download

Download the [production version][min] or the [development version][max], or use a [package manager](#package-managers).

[min]: https://raw.github.com/fegemo/bespoke-simple-overview/master/dist/bespoke-simple-overview.min.js
[max]: https://raw.github.com/fegemo/bespoke-simple-overview/master/dist/bespoke-simple-overview.js

## Usage

This plugin is shipped in a [UMD format](https://github.com/umdjs/umd), meaning that it is available as a CommonJS/AMD module or browser global.

For example, when using CommonJS modules:

```js
var bespoke = require('bespoke'),
  overview = require('bespoke-simple-overview');

bespoke.from('#presentation', [
  overview()
]);
```

When using browser globals:

```js
bespoke.from('#presentation', [
  bespoke.plugins.overview()
]);
```

By default, bespoke-simple-overview uses the `Esc` key to activate/deactivate the
overview mode, but it can be changed using the option `activationKey`:

```js
bespoke.from('#presentation', [
  overview({
    activationKey: 'c'   // Defaults to ESC
  })
]);
```

## Package managers

### npm

```bash
$ npm install bespoke-simple-overview
```

### Bower

```bash
$ bower install bespoke-simple-overview
```

## Credits

This plugin was built with [generator-bespokeplugin](https://github.com/markdalgleish/generator-bespokeplugin).

## License

[MIT License](http://en.wikipedia.org/wiki/MIT_License)
