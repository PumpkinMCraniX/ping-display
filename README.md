# Ping Display — PumpkinMC Plugin

Shows each player's ping next to their name in the tab list, color-coded by quality.

| Ping      | Color  | Code |
|-----------|--------|------|
| 0–50 ms   | Green  | §a   |
| 51–100 ms | Yellow | §e   |
| 101–200 ms| Gold   | §6   |
| 200+ ms   | Red    | §c   |

## Requirements

- Rust toolchain (`rustup default stable`)
- WASM target: `rustup target add wasm32-wasip2`
- Pumpkin server **0.2.0+26.3-26.51** (API must match)

## Build

```bash
cargo build --release
```

Output:

```
target/wasm32-wasip2/release/ping_display.wasm
```

## Install

1. Copy `ping_display.wasm` into your Pumpkin server's `plugins/` folder.
2. Restart the server.

## Note

Pumpkin loads **WebAssembly** plugins (`.wasm`), not native `.so` / `.dll` libraries.
The dependency is pinned to tag `0.2.0+26.3-26.51` so the WIT API matches that server release.
