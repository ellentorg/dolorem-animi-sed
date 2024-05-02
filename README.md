# @ellentorg/dolorem-animi-sed <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Helper package to shim a method into `Array.prototype[Symbol.unscopables]`

## Example

```js
const assert = require('assert');

const shimUnscopables = require('@ellentorg/dolorem-animi-sed');

let copyWithin;
let concat;
with ([]) {
    assert.equal(concat, Array.prototype.concat);
    assert.notEqual(copyWithin, Array.prototype.copyWithin);
}

shimUnscopables('concat');

with ([]) {
    assert.notEqual(concat, Array.prototype.concat);
    assert.notEqual(copyWithin, Array.prototype.copyWithin);
}
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Security

Please email [@ljharb](https://github.com/ljharb) or see https://tidelift.com/security if you have a potential security vulnerability to report.

[package-url]: https://npmjs.org/package/@ellentorg/dolorem-animi-sed
[npm-version-svg]: https://versionbadg.es/ljharb/@ellentorg/dolorem-animi-sed.svg
[deps-svg]: https://david-dm.org/ljharb/@ellentorg/dolorem-animi-sed.svg
[deps-url]: https://david-dm.org/ljharb/@ellentorg/dolorem-animi-sed
[dev-deps-svg]: https://david-dm.org/ljharb/@ellentorg/dolorem-animi-sed/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@ellentorg/dolorem-animi-sed#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@ellentorg/dolorem-animi-sed.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@ellentorg/dolorem-animi-sed.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@ellentorg/dolorem-animi-sed.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@ellentorg/dolorem-animi-sed
[codecov-image]: https://codecov.io/gh/ljharb/@ellentorg/dolorem-animi-sed/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@ellentorg/dolorem-animi-sed/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@ellentorg/dolorem-animi-sed
[actions-url]: https://github.com/ellentorg/dolorem-animi-sed/actions
