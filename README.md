# MITMFuzz
On the fly TCP and UDP network fuzzer

Performs random BoF, IoF, IuF, format string injection, null byte injection, and bitflipping on mutated packets, at random offsets. For best results, put your test packet generator on a loop, and wait for crashes.

### Usage

python mitmfuzz -l <localport> -r <remotehost> -p <remoteport> [options]

[options]
-c: Fuzz only client side (both otherwise)
-s: Fuzz only server side (both otherwise)
-w: Number of requests to send before start fuzzing
-u: UDP protocol (otherwise TCP is used)
-v: Verbose (outputs network traffic)
-h: Help page

Modify the "overflowstrings" array to add in your own BoF payloads.
Modify the "fuzz(data)" function to change the fuzzing logic
