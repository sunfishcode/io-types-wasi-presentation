# Compatibility with existing code

A libc mode that uses I/O streams and I/O arrays will be able to support:
  - `read`, `write`, `pread`, `pwrite`
    - and everything build around them
  - all non-I/O things
  - `lseek`
  - Emulation for `open`, `mmap`, `socket`, etc.

Continue to support the libc mode that uses wasi-filesystem and wasi-sockets.

Let developers chose!
