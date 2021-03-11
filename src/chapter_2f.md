# Errors

Report partial success along with failure.
 - Wasm has multiple return values!

Error types:
 - Applications usually don't care why `read` or `write` failed
 - Detailed errors expose host information
 - Options:
    - Success/Failure
    - Opaque handle

No `EINTR`
 - Wasm has no signals! 😎
 - No need to wrap `read` and `write` in retry loops

Don't be a file or a socket API:
 - Errors and `EOF` are sticky!
 - No `ETIMEDOUT`
 - Atomicity? Seek higher-level APIs that preserve intent
