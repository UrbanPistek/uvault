# Rust
Rust book - https://doc.rust-lang.org/book/ch01-01-installation.htm
Operating system in rust - https://www.redox-os.org/
[Practice](https://exercism.org/tracks/rust)

#### Build: 
`rustc <name>.rs`

Specify output dir of binary
`rustc <name>.rs --out-dir <>`

#### Cargo

Create new cargo project 
`cargo new <name>`

Cargo assumes a project structure as follows: 
```
├── Cargo.lock
├── Cargo.toml
├── src
│   └── main.rs
└── target
```

It looks for source files to compile under the `src` directory. 

Check code for compile errors:
`cargo check`

Run and build with cargo:
`cargo build`
`cargo run`
