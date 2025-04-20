# Setup Rust & Toolchain

Action to install and configure Rust in a Github Action workflow.
Works **ONLY** with [Github Action](https://github.com/features/actions).

## Usage

```yaml
- id: setup-rust
  uses: nebetoxyz/setup-rust--action@v1.2.0
  with:
    # Used to specify a package manager for caching in the default directory.
    # Supported values : cargo
    cache: "cargo"
    # Used to specify components to install.
    # Supported values : rustfmt, rust-docs, rust-analyzer, clippy, llvm-tools.
    components: "rustfmt,rust-docs,rust-analyzer,clippy,llvm-tools"
```

## Samples

### Setup Rust without cache

```yaml
- id: setup-rust
  uses: nebetoxyz/setup-rust--action@v1.2.0
```

### Setup Rust with cache on Cargo dependencies

```yaml
- id: setup-rust
  uses: nebetoxyz/setup-rust--action@v1.2.0
  with:
    cache: "cargo"
```

### Setup Rust with [LLVM](https://llvm.org/) component for [coverage](https://doc.rust-lang.org/beta/rustc/instrument-coverage.html)

```yaml
- id: setup-rust
  uses: nebetoxyz/setup-rust--action@v1.2.0
  with:
    components: "llvm-tools"
```

## Contact

For any question or feature suggestion, you can take a look and open, if necessary, a new [discussion](https://github.com/nebetoxyz/setup-rust--action/discussions).

For any bug, you can take a look to our active issues and open, if necessary, a new [issue](https://github.com/nebetoxyz/setup-rust--action/issues).
