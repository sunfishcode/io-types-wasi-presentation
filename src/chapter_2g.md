# Relationship to filesystem and sockets

The wasi-filesystem and (anticipated) wasi-sockets proposals will continue:
 - Now with less pressure to provide perfect portability
 - Can now more easily expand in scope

Some use cases will always need the extra functionality of wasi-filesystem
and wasi-sockets.

Some host environments won't support that functionality.

WASI can accommodate both.
