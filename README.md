<p align="center">
  <a href="https://github.com/ChuMicro/ChuMicro"><img src="https://raw.githubusercontent.com/ChuMicro/ChuMicro/main/support/docs/chumicro.png" width="420" alt="ChuMicro" /></a>
</p>
<h1 align="center">ChuMicro-Bundle-Experimental</h1>

<p align="center">
  <strong>Experimental bundle for <a href="https://github.com/ChuMicro/ChuMicro">ChuMicro</a> &mdash; install any library on CircuitPython, MicroPython, or CPython.</strong>
</p>

<p align="center">
  <a href="https://chumicro.github.io/ChuMicro/">Docs</a> &bull;
  <a href="https://github.com/ChuMicro/ChuMicro">Source</a> &bull;
  <a href="https://github.com/ChuMicro/ChuMicro-Bundle">Stable Bundle</a>
</p>

> ⚠️ **Pre-release channel** — these builds come from `main` and may contain breaking changes.


## Get started

Swap `chumicro-timing` for whichever library you need.

**CircuitPython ([circup](https://github.com/adafruit/circup)):**

[circup](https://github.com/adafruit/circup) is CircuitPython's package manager — it uses bundles to find third-party packages. Register the ChuMicro bundle once, then install any library by name:

```bash
circup bundle-add ChuMicro/ChuMicro-Bundle-Experimental
circup install chumicro-timing
```

> If you previously registered the stable bundle, remove it first — circup may pick either version when both are active:
> ```
> circup bundle-remove ChuMicro/ChuMicro-Bundle
> ```

**MicroPython ([mip](https://docs.micropython.org/en/latest/reference/packages.html)):**

```bash
mpremote mip install github:ChuMicro/ChuMicro-Bundle-Experimental/chumicro_timing
```

Or from the REPL on a network-capable board:

```python
import mip
mip.install("github:ChuMicro/ChuMicro-Bundle-Experimental/chumicro_timing")
```

> **Want pre-compiled `.mpy` bytecode?** Add `mpy6/` before the package name for faster startup and lower RAM usage on boards with mpy format v6 (MicroPython 1.24+, CircuitPython 10.x):
> ```
> mpremote mip install github:ChuMicro/ChuMicro-Bundle-Experimental/mpy6/chumicro_timing
> ```

**CPython (pip):**

On your laptop, install from PyPI — no bundle needed:

```bash
pip install chumicro-timing-experimental
```

## What's in the bundle?

| Library | Version | Description |
| --- | --- | --- |
| [**chumicro-compat**](https://github.com/ChuMicro/ChuMicro/tree/main/libraries/compat) | 0.1.19 | Cross-runtime compatibility polyfills for CircuitPython, MicroPython, and CPython — functools.partial and more. |
| [**chumicro-msgpack**](https://github.com/ChuMicro/ChuMicro/tree/main/libraries/msgpack) | 0.1.19 | Compact MessagePack serialization for CircuitPython, MicroPython, and CPython — delegates to the native C module when available. |
| [**chumicro-runner**](https://github.com/ChuMicro/ChuMicro/tree/main/libraries/runner) | 0.1.19 | Tick-based task runner for CircuitPython, MicroPython, and CPython — non-blocking check/handle scheduling without async. |
| [**chumicro-timing**](https://github.com/ChuMicro/ChuMicro/tree/main/libraries/timing) | 0.1.19 | Wraparound-safe millisecond tick helpers and heartbeat scheduling for CircuitPython, MicroPython, and CPython. |

Each directory contains `.py` source, `.mpy` bytecode (CircuitPython 10.x, mpy v6), and a `package.json` manifest for mip.

## About

This repo is generated automatically by the [ChuMicro release workflow](https://github.com/ChuMicro/ChuMicro/blob/main/.github/workflows/release.yml). Don't edit it by hand — changes will be overwritten on the next release.

- **Source code and examples:** [ChuMicro/ChuMicro](https://github.com/ChuMicro/ChuMicro)
- **Documentation:** [chumicro.github.io/ChuMicro](https://chumicro.github.io/ChuMicro/)
- **Stable bundle:** [ChuMicro/ChuMicro-Bundle](https://github.com/ChuMicro/ChuMicro-Bundle)
- **License:** [MIT](LICENSE)
