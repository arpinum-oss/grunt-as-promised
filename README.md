# Grunt as promised [![Build Status](https://travis-ci.org/arpinum-oss/grunt-as-promised.svg?branch=master)](https://travis-ci.org/arpinum-oss/grunt-as-promised)

> If you wish to be a success in the world, promise everything, deliver nothing.
> <cite>(Napoleon Bonaparte)</cite>

**Grunt as promised** helps you write async custom tasks through promises

## Installation

    npm install grunt-as-promised --save-dev

## Usage

Require `grunt-as-promised` in your `Gruntfile.js`:

```javascript
var gap = require('grunt-as-promised');
```

Then define tasks as functions returning a promise:

```javascript
module.exports = function (grunt) {
  gap.registerTask(grunt, 'inline', function () {
    return doSomething().then(function() {
      return doSomethingElse();
    });
  });
};
```

## Examples

Some examples are available in [examples](https://github.com/arpinum-oss/grunt-as-promised/tree/master/examples).

## License

[MIT](LICENSE)
