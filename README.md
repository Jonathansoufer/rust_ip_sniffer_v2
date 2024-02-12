## Port Scanner in Rust
This is a simple, yet efficient, port scanner written in Rust. It uses the tokio library for asynchronous programming and the bpaf library for command line argument parsing.

# Features
- Asynchronous port scanning
- Customizable IP address and port range
- Efficient error handling

# Usage
The program accepts the following command line arguments:

- `-a` or `--address: The IP address that you want to scan. It must be a valid IPv4 address. If not provided, it defaults to `127.0.0.1`.
- `-s` or `--start`: The start port for the scan. It must be greater than `0`. If not provided, it defaults to `1`.
- -e or --end: The end port for the scan. It must be less than or equal to `65535`. If not provided, it defaults to `65535`.

# Example

```bash
cargo run -- -a 192.168.1.1 -s 1 -e 1024
```

This command will scan the IP address `192.168.1.1` from port `1` to port `1024`.

# Output
The program prints a . for each port it scans. If a port is open, it will print a message in the format port is open.

# Building
To build the program, you need to have Rust installed. You can build the program using the following command:

```bash
cargo build --release
```

This will create an executable in the `target/release` directory.

