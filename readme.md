# f_ck

Clean-up cuss words.

## Contents

*   [What is this?](#what-is-this)
*   [When should I use this?](#when-should-i-use-this)
*   [Install](#install)
*   [Use](#use)
*   [API](#api)
    *   [`vowel(value[, character])`](#vowelvalue-character)
    *   [`inner(value[, character])`](#innervalue-character)
    *   [`grawlix(value[, pattern])`](#grawlixvalue-pattern)
*   [Types](#types)
*   [Compatibility](#compatibility)
*   [Security](#security)
*   [Related](#related)
*   [Contribute](#contribute)
*   [License](#license)

## What is this?

This package provides three ways to clean obscene strings: vowels (`c*ss`),
inner letters (`c**s`), and grawlix (`@#$%`).

> Not affiliated with Football Club København.

## When should I use this?

Maybe when you have some cuss words in your tests that you’re tired of looking
at?

## Install

This package is [ESM only][esm].
In Node.js (version 14.14+, 16.0+), install with [npm][]:

```sh
npm install f-ck
```

In Deno with [`esm.sh`][esmsh]:

```js
import * as fck from 'https://esm.sh/f-ck@2'
```

In browsers with [`esm.sh`][esmsh]:

```html
<script type="module">
  import * as fck from 'https://esm.sh/f-ck@2?bundle'
</script>
```

## Use

```js
import {vowel, inner, grawlix} from 'f-ck'

console.log(vowel('butt')) // => 'b*tt'
console.log(inner('butt')) // => 'b**t'
console.log(grawlix('butt')) // => '@#$%'
console.log(grawlix(7)) // => '@#$%!&?'

console.log(vowel('butt', '-')) // => 'b-tt'
```

## API

This package exports the identifiers `vowel`, `inner`, and `grawlix`.
There is no default export.

### `vowel(value[, character])`

Sanitize `value` (`string`) by replacing vowels in `value` with `character`
(`string`, default: `'*'`).

### `inner(value[, character])`

Sanitize `value` (`string`) by replacing all characters except the first and
last in `value` with `character` (`string`, default: `'*'`).

### `grawlix(value[, pattern])`

Sanitize `value` (`string` or `number`) using a [grawlix][] pattern (`string`,
default: `'@#$%!&?'`).
Essentially, repeats `pattern` for `value` (when `number`) or `value.length`
(when `string`) characters.

## Types

This package is fully typed with [TypeScript][].
It exports no additional types.

## Compatibility

This package is at least compatible with all maintained versions of Node.js.
As of now, that is Node.js 14.14+ and 16.0+.
It also works in Deno and modern browsers.

## Security

This package is safe.

## Related

*   [`profanities`][profanities]
    — list of (possible) English profane words
*   [`cuss`][cuss]
    — map of English profane words to a rating of sureness

## Contribute

Yes please!
See [How to Contribute to Open Source][contribute].
