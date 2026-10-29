# curl / libcurl - llm port

Original project: [curl / libcurl](https://github.com/curl/curl), version 8.23.0.
Original authors: Daniel Stenberg and the curl contributors. [Original repository](https://github.com/curl/curl).

The library is the work of its original authors, not a product of llm-build-system.
This repository only maintains its llm build integration and source subset,
it is not an official upstream release. Upstream source and header files are
unchanged. Build configuration files added by this port are kept separately.
Upstream build systems, command-line tools, tests and manuals are omitted.

The original license is preserved verbatim in [LICENSE](LICENSE).
[Upstream license](https://github.com/curl/curl/blob/curl-8_23_0/COPYING). Copyright and per-file license notices
remain in the original files.

Additional upstream copyright and license notices from the included source
files are reproduced verbatim in [NOTICE](NOTICE) for binary redistribution.
The original notices remain in the source files.

Build the static library with `llm build --release`. Consumers include
`<curl/curl.h>`. zlib 1.3.2 is used on all platforms. Linux and macOS also
use OpenSSL 3.5.9. Dependencies are pinned in the
[llm registry](https://github.com/llm-build-system/llm-registry).
Windows uses curl's Schannel backend with Windows certificate validation.
Linux and macOS use curl's OpenSSL backend. LDAP/LDAPS and optional
HTTP/2, HTTP/3, SSH, Brotli and Zstandard integrations are not enabled.
Platform configuration profiles target the five native llm SDK targets.
