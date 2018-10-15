# binreader - BinaryReader for Python

A BinaryReader class for Python 3.6+.


## Usage

### binreader.BinaryReader

Instanciate a BinaryReader class:

```py
from binreader import BinaryReader

with open("example.bin", "rb") as f:
	reader = BinaryReader(f)
	print(reader.read_int())  # Reads an int32, returns a Python int
```

The following read methods are available:

- `read_bool()` -> `bool`
- `read_byte()` -> `int`
- `read_ubyte()` -> `int`
- `read_int16()` -> `int`
- `read_uint16()` -> `int`
- `read_int32()` -> `int`
- `read_uint32()` -> `int`
- `read_int64()` -> `int`
- `read_uint64()` -> `int`
- `read_int()` -> `int` (alias of `read_int32()`)
- `read_uint()` -> `int` (alias of `read_uint32()`)
- `read_float()` -> `float`
- `read_double()` -> `float`

The following string read methods are available:

- `read_cstring()` -> `bytes`: Reads a null-terminated string.
- `read_string(size: int=None)` -> `str`: Reads and decodes a string of size `size`. If `size` is `None`, expects a null terminator.

The following utility methods are available:

- `align()`: Seeks forward to align the buffer's handle position on a multiple of 4 bytes.
- `read(*args)`: Calls `read(*args)` on the buffer.
- `seek(*args)`: Calls `seek(*args)` on the buffer.
- `tell()`: Returns the buffer's handle position.


## License

This project is licensed under the MIT license. The full license text is
available in the LICENSE file.
