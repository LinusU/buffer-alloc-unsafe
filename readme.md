# Buffer Alloc Unsafe

A ponyfill for `Buffer.allocUnsafe`.

## Installation

```sh
npm install --save buffer-alloc-unsafe
```

## Usage

```js
const allocUnsafe = require('buffer-alloc-unsafe')

console.log(allocUnsafe(10))
//=> <Buffer 78 0c 80 03 01 00 00 00 05 00>

console.log(allocUnsafe(10))
//=> <Buffer 58 ed bf 5f ff 7f 00 00 01 00>

console.log(allocUnsafe(10))
//=> <Buffer 50 0c 80 03 01 00 00 00 0a 00>

allocUnsafe(-10)
//=> RangeError: "size" argument must not be negative
```

## API

### allocUnsafe(size)

- `size` &lt;Integer&gt; The desired length of the new `Buffer`

Allocates a new *non-zero-filled* `Buffer` of `size` bytes. The `size` must be
less than or equal to the value of `buffer.kMaxLength` and greater than or equal
to zero. Otherwise, a `RangeError` is thrown.

## See also

- [buffer-alloc](https://github.com/LinusU/buffer-alloc) A ponyfill for `Buffer.alloc`
- [buffer-from](https://github.com/LinusU/buffer-from) A ponyfill for `Buffer.from`
