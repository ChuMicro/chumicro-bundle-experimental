# ChuMicro-Bundle-Experimental

> ⚠️ **Pre-release channel** — these builds come from the `develop` branch and may contain breaking changes.

Experimental distribution bundle for [ChuMicro](https://github.com/ChuMicro/ChuMicro) libraries.  Contains `.py` source, `.mpy` bytecode, and `package.json` manifests for [mip](https://docs.micropython.org/en/latest/reference/packages.html) and [circup](https://github.com/adafruit/circup) installation.

## Installation

### CircuitPython (circup)

Remove any other ChuMicro bundle first, then register this one:

```bash
circup bundle-remove ChuMicro/ChuMicro-Bundle   # skip if stable was never added
circup bundle-add ChuMicro/ChuMicro-Bundle-Experimental
circup install chumicro-timing   # example
```

### MicroPython (mip)

Install directly from the bundle repo:

```bash
mpremote mip install github:ChuMicro/ChuMicro-Bundle-Experimental/chumicro_timing   # example
```

Or on a network-capable board:

```python
import mip
mip.install("github:ChuMicro/ChuMicro-Bundle-Experimental/chumicro_timing")   # example
```

### CPython (pip)

CPython users install from PyPI — the bundle repo is not involved:

```bash
pip install chumicro-timing-experimental   # example
```

## Available libraries

| Library | Version | Description |
| --- | --- | --- |
| [**chumicro-compat**](https://github.com/ChuMicro/ChuMicro/tree/develop/libraries/compat) | 0.1.6 | Cross-runtime compatibility polyfills for CPython, MicroPython, and CircuitPython. |
| [**chumicro-msgpack**](https://github.com/ChuMicro/ChuMicro/tree/develop/libraries/msgpack) | 0.1.6 | Cross-runtime [MessagePack](https://msgpack.org) serialization for CircuitPython, MicroPython, and CPython. |
| [**chumicro-runner**](https://github.com/ChuMicro/ChuMicro/tree/develop/libraries/runner) | 0.1.6 | Tick-based task runner with shared timestamps for Chumicro applications. |
| [**chumicro-timing**](https://github.com/ChuMicro/ChuMicro/tree/develop/libraries/timing) | 0.1.6 | Cross-runtime millisecond tick helpers and periodic timing utilities. |

Each library directory in this repo contains a `package.json` manifest for mip, `.py` source files, and `.mpy` compiled bytecode (CircuitPython 10.x, mpy format v6).

## About

This repository is **automatically maintained** by the [ChuMicro source repo](https://github.com/ChuMicro/ChuMicro)'s release workflow.  Do not edit it manually.

- **Source code, docs, and examples:** [ChuMicro/ChuMicro](https://github.com/ChuMicro/ChuMicro)
- **Stable bundle:** [ChuMicro/ChuMicro-Bundle](https://github.com/ChuMicro/ChuMicro-Bundle)
- **License:** [MIT](https://github.com/ChuMicro/ChuMicro/blob/develop/LICENSE)
