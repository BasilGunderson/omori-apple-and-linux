# Technical Writeup on the OMORI Mac arm64/x64 patch

## Quick outline
* Repackage omori into nw.js [v0.106.1](https://dl.nwjs.io/v0.106.1/)
* Update steamworks to 1.53a (`libsteam_api.dylib` and `libsdkencryptedappticket.dylib`)
* Patch [greenworks](https://github.com/SnowpMakes/greenworks-arm64) to compile to arm64 with steamworks 1.53a
* Alternatively, patch [greenworks](https://github.com/greenheartgames/greenworks) to compile to x64 with steamworks 1.53a
* Polyfill node included with nw.js v0.106.1 to restore deprecated support for writing raw number types to files causing [a bug](https://github.com/SnowpMakes/omori-apple-silicon/issues/1).

