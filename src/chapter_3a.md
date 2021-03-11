# Are files I/O Streams or I/O Arrays?

Both! (like POSIX)

With separate handles! (unlike POSIX)

What about `lseek`?
 - POSIX `lseek` bridges between array and stream
 - Emulate `lseek` in libc
