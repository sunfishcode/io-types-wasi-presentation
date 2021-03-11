# I/O Streams

Overview:
  - Reliable in-order delivery of bytes
    - or in the future, of arbitrary type
  - Examples: sockets, pipes, character devices, files\*
  - Prototype: <https://crates.io/crates/io-streams>, <https://crates.io/crates/nameless>

Operations:
  - `read` (input)
  - `write` (output)
  - `skip` (input) - like `read` but discards data
  - `write_zeros` (output) - like `write` but just writes zeros
  - `flush` (output) - flush buffers, report errors
  - `media_type` - return a `string` with the IANA Media Type (eg. "image/jpeg")
  - `pseudonym` - return a handle to an identifier
  - `write_pseudonym` - (output) write the name of a pseudonym to the output
  - `forward` - `read` from an input and `write` the data to another 💨

Constructors:
  - `pipe`
  - `null` - (output) bit bucket
  - `from_array` - form a stream from an I/O array at a given offset
