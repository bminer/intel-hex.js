# intel-hex.js

A parser/writer for Intel HEX file format.

## Usage

```js
require("intel_hex").parse(data);
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

Special thanks to: http://en.wikipedia.org/wiki/Intel_HEX
