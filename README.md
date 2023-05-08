# WinpkFilter Rust POC

### References 

- [listadapters](https://github.com/firezone/ndisapi/blob/main/examples/listadapters.rs)
- [passthru.rs](https://github.com/firezone/ndisapi/blob/main/examples/passthru.rs)

## Usage

1. Use `cargo run --bin adapter` to get list of adapters
2. `cargo run --bin network -- --interface-index 2 --packets-number 150` where 2 is my wifi card connection
