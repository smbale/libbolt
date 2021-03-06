# libbolt

A pure-Rust library implementation of BOLT: Blind Off-chain Lightweight Transactions.

BOLT is a system for conducting privacy-preserving off-chain payments between pairs of individual parties. BOLT is designed to provide a Layer 2 payment protocol for privacy-preserving cryptocurrencies such as Zcash, by allowing individuals to establish and use payment channels for instantaneous payments that do not require an on-chain transaction.

# WARNING

The libbolt library is a proof of concept implementation that relies on experimental libraries and dependencies at the moment. It is not suitable for production software yet.

# Dependencies

* secp256k1
* sodiumoxide
* bn
* bulletproofs

Note that the above rust dependencies will be compiled and installed as a result of running the `make` command.

# Rust Nightly Setup

Please keep in mind we are currently working with nightly Rust for now which gives access to the nightly compiler and experimental features.

	rustup install nightly
	
To run a quick test of the nightly toolchain, run the following command:

	rustup run nightly rustc --version

Optionally, to make this the default globally, run the following command:

	rustup default nightly

We will switch to the stable release channel once libbolt (and dependencies) are ready for production use.

# Build & Install

Please ensure you have installed the libsodium library for your platform. See install instructions [here](https://download.libsodium.org/doc/installation/index.html).

To build the library and execute basic tests, run `make` 

# Tests

To run libbolt unit tests, run `make test`

# Benchmarks

To run libbolt benchmarks, run `make bench`

# Usage

To use the libbolt library, add the `libbolt` crate to your dependency file in `Cargo.toml` as follows:

```toml
[dependencies]
libbolt = "0.1.0"
```

Then add an extern declaration at the root of your crate as follows:
```rust
extern crate libbolt;
```

# API

The libbolt library provides APIs for three types of privacy-preserving payment channels:

* unidirectional payment channels (*work in progress*)
* bidirectional payment channels (done)
* third-party payments (done)

## Bidirectional Payment Channels

**TODO**

## Third-party Payment Support

**TODO**

# Documentation

Build the api documentation by simply running `make doc`. Documentation will be generated in your local `target/doc` directory.

For the libbolt design documentation, see the `docs/bolt_design.pdf` document.

# Contributions

To contribute code improvements, please checkout the repository, make your changes and submit a pull request.

	git clone https://github.com/yeletech/libbolt.git

	
# License

Licensed under MIT (LICENSE-MIT or http://opensource.org/licenses/MIT)
