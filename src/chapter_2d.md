# I/O Arrays

Overview:
  - Dynamic array of bytes
    - or in the future, of arbitrary type
  - Examples: disk partitions, memory buffers, device memory, files\*
  - Prototype: <https://crates.io/crates/io-arrays>

Operations:
  - `read_at`
  - `write_at`
  - `len` - current length
  - `set_len` - set current length, truncating or appending zeros
  - `advise` - optimization hints
  - `flush` - flush buffers, report errors
  - `media_type` - return a `string` with the IANA Media Type (eg. "image/jpeg")
  - `pseudonym` - return a handle to an identifier
  - `copy` - `read_at` from one I/O array and `write_at` the data to another 💨

Constructors:
  - `anonymous`
  - `from_stream` - read all the data from an input stream and write it into an anonymous I/O array
