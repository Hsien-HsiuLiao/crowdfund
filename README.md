install solana cli
```
sh -c "$(curl -sSfL https://release.solana.com/v1.10.8/install)"

export PATH="/home/gitpod/.local/share/solana/install/active_release/bin:$PATH"

solana-test-validator

solana-keygen new --no-bip39-passphrase -o keypair.json

solana config set --keypair keypair.json

solana config set --url http://127.0.0.1:8899

cargo build-bpf --manifest-path=./rust/Cargo.toml

solana program deploy ./rust/target/deploy/crowdsource.so

```

## sanity check and transferring money

```
solana account <enter the above displayed address>, ex: 3jm8yUPZ3HxmCUjoTn8sRh5kPppEfwTgQmNHZYZsoqfk
```