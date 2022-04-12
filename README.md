install solana cli

sh -c "$(curl -sSfL https://release.solana.com/v1.10.8/install)"

export PATH="/home/gitpod/.local/share/solana/install/active_release/bin:$PATH"

solana-test-validator

solana-keygen new

solana config set --url http://127.0.0.1:8899

cargo build-bpf --manifest-path=./rust/Cargo.toml

solana program deploy ./rust/target/deploy/crowdsource.so
