# WinpkFilter Rust POC

### References 

- [listadapters](https://github.com/firezone/ndisapi/blob/main/examples/listadapters.rs)
- [passthru.rs](https://github.com/firezone/ndisapi/blob/main/examples/passthru.rs)

## Usage

1. Use `cargo run --bin adapter` to get list of adapters
   > This example demonstrates the basic usage of the `Ndisapi` object, `Ndisapi::get_tcpip_bound_adapters_info`, adapter name conversion functions, and `Ndisapi::get_mtu_decrement` and etc.. It retrieves information about the network interfaces, including their indexes, which can be passed to the `packthru` and `passthru` examples. The collected information is dumped to the console screen.
2. `cargo run --bin network -- --interface-index 2 --packets-number 150` where 2 is my wifi card connection
   > This example demonstrates the essential usage of active filtering modes for packet processing. It selects a network interface and sets it into a filtering mode, where both sent and received packets are queued. The example registers a Win32 event using the `Ndisapi::set_packet_event` function, and enters a waiting state for incoming packets. Upon receiving a packet, its content is decoded and displayed on the console screen, providing a real-time view of the network traffic.
