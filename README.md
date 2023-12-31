[package]
name = "memory-socket"
version = "0.2.0"
description = "In-memory socket abstraction"
documentation = "https://docs.rs/memory-socket"
repository = "https://github.com/bmwill/memory-socket"
authors = ["Brandon Williams <bwilliams.eng@gmail.com>"]
license = "MIT OR Apache-2.0"
readme = "README.md"
edition = "2018"

[dependencies]
bytes = "0.5"
flume = { version = "0.7", default-features = false }
futures = { version = "0.3", optional = true }
once_cell = "1.3"

[features]
# Include nothing by default
default = []

# enable async support
async = ["futures", "flume/async"]

[[test]]
name = "async"
required-features = ["async"]

[package.metadata.docs.rs]
all-features = true# Cargo.toml
