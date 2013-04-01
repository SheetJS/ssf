# SSF

SpreadSheet Format (SSF) is a pure-JS library to format data using ECMA-376 
spreadsheet format codes (like those used in Microsoft Excel)

This is written in [voc](https://npmjs.org/package/voc) -- see ssf.md for code.

To build: `voc ssf.md`

## Setup

In the browser:

    <script src="ssf.js"></script>

In node:

    var SSF = require('ssf');

## Usage

`.load(fmt, idx)` sets custom formats (generally indices above `164`)

`.format(fmt, val)` formats `val` using the format `fmt`.  If `fmt` is of type
`number`, the internal table (and custom formats) will be used.  If `fmt` is a
literal format, then it will be parsed and evaluated.

## Notes

Format code 14 in the spec is broken; the correct format is 'mm/dd/yy' (dashes,
not spaces)

## License

```
Copyright (C) 2013 Niggler

The MIT License (MIT)

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in 
the Software without restriction, including without limitation the rights to 
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies 
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all 
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR 
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE 
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER 
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, 
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE 
SOFTWARE.


Except where noted, this license applies to any and all software programs and 
associated documentation files created by the Original Author and distributed 
with the Software.
```
