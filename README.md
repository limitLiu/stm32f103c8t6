# STM32F103C8T6

## Start

To build embedded programs using this template you'll need:

- Rust 1.79 or a newer toolchain. e.g. `rustup default nightly`

- The `cargo generate` subcommand. [Installation
  instructions](https://github.com/ashleygwilliams/cargo-generate#installation).

- `rust-std` components (pre-compiled `core` crate) for the ARM Cortex-M
  targets. Run:

```console
$ rustup target add thumbv7m-none-eabi
```

## Run

```console
$ cargo build --release
$ openocd -f openocd.cfg -c "program target/thumbv7m-none-eabi/release/stm32f103c8t6 reset exit 0x08000000"
```
