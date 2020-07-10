# Substrate Permissioning Samples

A [Substrate](https://github.com/paritytech/substrate) node template based sample runtime, showcasing validator and account permissioning.

## Permissioning Pallets

The runtime includes:

* [Account Set pallet](https://github.com/gautamdhameja/substrate-account-set) for account-level permissioning using account allow-list.
* [Validator Set pallet](https://github.com/gautamdhameja/substrate-validator-set) for managing addition and removal of validators in PoA networks.

## Build

Install Rust:

```bash
curl https://sh.rustup.rs -sSf | sh
```

Initialize your Wasm Build environment:

```bash
./scripts/init.sh
```

Build Wasm and native code:

```bash
cargo build --release
```

## Run

Start a development chain with:

```bash
./target/release/substrate-permissioning --dev
```

Detailed logs may be shown by running the node with the following environment variables set: `RUST_LOG=debug RUST_BACKTRACE=1 cargo run -- --dev`.

## Disclaimer

This code not audited and reviewed for production use cases. You can expect bugs and security vulnerabilities. Do not use it as-is in real applications.
