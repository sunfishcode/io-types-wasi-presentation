# Zero copy

- Ways to do zero-copy
  - `forward`, `skip`, `write_zeros`, `copy`
  - `io-array`'s `read_at` skips intervening data
  - create an I/O Array and pass around a handle
- `read` is not zero-copy
  - shared pages require protocols, synchronization
    - not virtualizable
- What can we do instead?
  - Avoid bringing data into an instance that doesn't need it
  - Use direct calls instead of shared-memory protocols where appropriate
