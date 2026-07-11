# libtnsl

The official implimentation of the TNSL Standard Library

`libtnsl` is a "batteries included" standard library which aims to keep these batteries as small as possible.

To that end there are a variety of modules, some of which may be omitted for smaller but less capable distributions of the standard library.

---
## Module Groups

Modules are grouped into `base`, `net`, or `full` groupings.  Base is the core modules provided, net adds networking, and full is the complete set including graphics and audio.

## Available Modules By Group

### Base Modules
* `algo`
  * common algorithms which act on types implementing the common library interfaces
* `box`
  * common container types implementing the common library interfaces
* `crypto`
  * cryptographic hash functions
  * cryptographic keygen
  * cryptographic signature generation and validation
  * encryption and decryption standards
* `encoding`
  * various data encoding types
  * various file encoding helpers
* `internal`
  * internal helpers for the library, not exported
* `io`
  * streaming input and output for a variety of common operations
  * file streaming helpers
  * memory streaming
  * device event streaming interface
  * various protocols
* `lang`
  * language constants
  * any language feature support which relies on the std library lives here
  * common interfaces used throughout the rest of the library
* `math`
  * common math functions
  * statistics
  * vector and matrix types
  * big number types
* `parallel`
  * threading
  * atomic primitives
  * locking primitives
  * threadsafe container types
  * greenthread support for yield funcs as well as default scheduler implementation
* `random`
  * prng for average use cases
  * cryptographic prng
  * access to sources of randomness
* `text`
  * text encoding and decoding
* `time`
  * time bases
  * timestamps
  * time formatting and translation between timezones
  * system clock access
  * timers

### Net Modules
* `net`
  * support for io pipes to TCP, UDP, and RAW internet sockets
  * support for TLS using the base `crypto` module
  * support for HTTP 1/2/3 protocol
  * support for WebSockets
  * support for a variety of other internet protocols

### Full Modules
* `audio`
  * support for audio playback through a graph based api with inputs, outputs, and transformers
  * audio transformer and generator protocols
  * support for a variety of sound formats
  * support for loading sound formats from files
* `graphics`
  * basic windowing support
  * light wrappers over a variety of low level graphics libraries
    * OpenGL
    * OpenXR
    * Vulkan
  * direct draw into window buffers
* `ui`
  * platform native UI engine
  * similar to win forms, GTK, Qt, etc. has structured dialog and window layouts
  * provides a default main event loop which calls to recievers

