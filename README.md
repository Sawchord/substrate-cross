# Cross Compilation of Parity Substrate

This repository contains informations and tools to enable crosscompilation of a Parity Substrate node.

It makes use of Cargso `cross` tool.

**This is a WIP and I will add new targets as I see fit. Pull requests welcome**

## How to use

Assuming you have already set up your Rust toolchain, you need to
do the following steps:

1. Install Cross:

    cargo install cross --force

2. Copy the `Cargo.toml` file from this directory into your projects main directory. It is the same as place, where your 
top `Cargo.toml` lives.

3. To compile the project using `cross build --relase --targetarmv7-unknown-linux-gnueabihf`.

**NOTE: This project only manages the build of the native 
binary cross-plattform. Rebuilding the runtime in `wasm` is
still done via the build script, provided by your nodes**

## How to rebuild the image:

The images need to be tagged accordingly, for `cross` to be able
to find them.
From the main directory of this project, run:

- armv7-unknown-linux-gnueabihf:

    docker build -t substrate-cross:armv7-unknown-linux-gnueabihf substrate-armv7-unknown-linux-gnueabihf/