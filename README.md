# Subspace Regenesis Tool

A command line tool to snapshot the balances state at any block of Subspace network for the incentivized testnet regenesis purpose, only the accounts created after the genesis block are recorded.

## Usage

```bash
# Export the latest balances state by connecting to a local node.
$ cargo run -- --url ws://127.0.0.1:9944

# Export the latest balances state at block 100
$ cargo run -- --url ws://127.0.0.1:9944 --block-number 100
```

A JSON file will be generated under the current directory, which contains all the exported balances and can be used to initialize the genesis state of new network.

Run `cargo run -- --help` to see all the usage.

## Upgrade Subspace metadata

Refer to https://github.com/paritytech/subxt#downloading-metadata-from-a-substrate-node for upgrading [`subspace_metadata.scale`](./subspace_metadata.scale) when necessary.
