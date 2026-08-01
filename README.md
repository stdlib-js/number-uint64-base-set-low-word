<!--

@license Apache-2.0

Copyright (c) 2026 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# setLowWord

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Set the low 32-bit word of a [64-bit unsigned integer][@stdlib/number/uint64/ctor].



<section class="usage">

## Usage

To use in Observable,

```javascript
setLowWord = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/number-uint64-base-set-low-word@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var setLowWord = require( 'path/to/vendor/umd/number-uint64-base-set-low-word/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/number-uint64-base-set-low-word@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.setLowWord;
})();
</script>
```

#### setLowWord( x, low )

Sets the low 32-bit word of a [64-bit unsigned integer][@stdlib/number/uint64/ctor].

```javascript
var getLowWord = require( '@stdlib/number-uint64-base-get-low-word' );
var Uint64 = require( '@stdlib/number-uint64-ctor' );

var a = new Uint64( 4294967296 );
// returns <Uint64>[ 4294967296n ]

var b = setLowWord( a, 2 );
// returns <Uint64>[ 4294967298n ]

var w = getLowWord( b );
// returns 2
```

</section>

<!-- /.usage -->

<section class="notes">

## Notes

-   The function returns a new [64-bit unsigned integer][@stdlib/number/uint64/ctor] instance without modifying the input value.

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/random-array-discrete-uniform@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/constants-uint32-max@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/number-uint64-ctor@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/console-log-each-map@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/number-uint64-base-set-low-word@umd/browser.js"></script>
<script type="text/javascript">
(function () {

var a = new Uint64( 4294967296 );
// returns <Uint64>

var words = discreteUniform( 100, 0, UINT32_MAX, {
    'dtype': 'uint32'
});

logEachMap( 'setLowWord(%s, %s) = %s', a, words, setLowWord );

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/number-uint64-base-set-low-word.svg
[npm-url]: https://npmjs.org/package/@stdlib/number-uint64-base-set-low-word

[test-image]: https://github.com/stdlib-js/number-uint64-base-set-low-word/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/number-uint64-base-set-low-word/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/number-uint64-base-set-low-word/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/number-uint64-base-set-low-word?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/number-uint64-base-set-low-word.svg
[dependencies-url]: https://david-dm.org/stdlib-js/number-uint64-base-set-low-word/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/number-uint64-base-set-low-word/tree/deno
[deno-readme]: https://github.com/stdlib-js/number-uint64-base-set-low-word/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/number-uint64-base-set-low-word/tree/umd
[umd-readme]: https://github.com/stdlib-js/number-uint64-base-set-low-word/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/number-uint64-base-set-low-word/tree/esm
[esm-readme]: https://github.com/stdlib-js/number-uint64-base-set-low-word/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/number-uint64-base-set-low-word/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/number-uint64-base-set-low-word/main/LICENSE

[@stdlib/number/uint64/ctor]: https://github.com/stdlib-js/number-uint64-ctor/tree/umd

<!-- <related-links> -->

<!-- </related-links> -->

</section>

<!-- /.links -->
