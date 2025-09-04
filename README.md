# acid64

A simple Rust CLI tool to decode Base64 and Base64URL-encoded strings.
Supports input from command-line arguments, files, or stdin.

## Features

- Decode standard Base64 or Base64URL
- Accept input from:
    - Command-line argument
    - File (`-f`)
    - Stdin (default fallback)
- Optional flag to ignore padding (`-p`)
- Output decoded result to stdout
- Graceful error handling

## Usage


# Decode standard Base64 from CLI
```shell
cargo run -- "SGVsbG8gd29ybGQ="
```

# Decode Base64URL from CLI
```shell
cargo run -- -u "YWJjZGVmZ2hpamtsbW5vcHFyc3R1dnd4eXotLS0_"
```

# Decode from file
```shell
cargo run -- -f input.txt
```

# Decode from stdin
```shell
echo "SGVsbG8gd29ybGQ=" | cargo run --
```

# Decode Base64URL from file, ignoring padding
```shell
cargo run -- -p "SGVsbG8td29ybGQ"
```
