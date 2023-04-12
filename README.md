# intel-hex.ts

A typescript-based parser/writer for the Intel Hex file format.
> This fork updates the package to use ES6 modules & TypeScript definitions.

## Installation
With `yarn`:
```bash
$ yarn add git+https://github.com/realjoshuau/intel-hex.ts.git
```

## Usage

```js
import { parse } from "intel-hex.ts"; // The module itself is named `intel-hex.ts`
```

The `parse` function takes 2 arguments:

- `data` - Intel Hex file (string in ASCII format or Buffer Object)
- `bufferSize` - the size of the Buffer containing the data (optional)

and returns an Object with the following properties:

- `data` - data as a Buffer Object, **padded with 0xFF
  where data is empty**.
- `startSegmentAddress` - the address provided by the last
  start segment address record; null, if not given
- `startLinearAddress` - the address provided by the last
  start linear address record; null, if not given

Special thanks to: http://en.wikipedia.org/wiki/Intel_HEX and [bminer/intel-hex.js](https://github.com/bminer/intel-hex.js)
