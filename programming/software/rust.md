# Rust
Rust book - https://doc.rust-lang.org/book/ch01-01-installation.htm
Operating system in rust - https://www.redox-os.org/
[Practice](https://exercism.org/tracks/rust)
Benchmarking: [Hyperfine](https://www.linode.com/docs/guides/installing-and-using-hyperfine-on-linux/)

#### Build: 
`rustc <name>.rs`

Specify output dir of binary
`rustc <name>.rs --out-dir <>`

## Basics
Rust executes first the code present inside the main function. Functions are wrapped in brackets and semicolons indicates the end of an experession. 
```
fn main(){

}
```

Running a function: `println()`  
Running a macro: `print()!` 
The `!` indicates a macro is being called. 

### Cargo
The rust build system and package manager. Creating a new project with `cargo new <name>` creates the directory, `Cargo.toml` , `src/main.rs` and if not within a git repository also initializes git. Cargo assumes all source files are within the `src` directory of the project. 

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

Use `cargo build --release` to build with optimizations, creates executable in `target/relase`

Before using any library in a program you will need to specify the dependancy in the `Cargo.toml` file: 
```
rand = "0.8.3"
```

### Variables
`let` : Creates a variable, immutable by default
`mut` : Makes a variable mutable 
`&` : Reference to variable, immutable by default. Can use `mut` to make it mutable as follows: `&mut val`
`const` : Constant, always immutable, need to be set to a constant expression and must be type annotated 
* Ex: `const VAL: u32 = 60;`

**Shadowing**
Re-declaring a variable:
```
let x = 5; 
// some code
let x = "string";
```

### Data Types 
Rust is statically typed, but it can often infer the value of the variable. To add a type annotation use `: <type>` Ex: `let val: u32 = 50;`

#### Scalar Types
- Integer
	- Can be signed: `i<size>`
	- Can be unsigned `u<size>
	- Size ranges from 8 - 128 bits, Ex: `u8`, `i64`, `u128`
	- Can specify to use computer architecture: `isize`, `usize` (most useful for indexing some collection)
	- The integer types default to `i32`
	- Literals: 
		- Hex: `0xff`
		- Octal: `0o77`
		- Binary: `0b11_00` (Note `_` is used as a visual seperator)
	- There are many methods for handling integer overflow in the standard library
- Floating Point
	- Either `f32` or `f64` , default is `f64`
- Boolean
	- Either `true` or `false`
- Character
	- Character literals are specified using single quotes`''`
	- 4 Bytes in size
	- Represents a unicode scalar value (which extends passed emojis all the value to emojis)

#### Compound Types
- Tuple: Bind multiple values of various types in a singular value
	- Ex: `let tup: (i32, f64, u8) = (9, 5.7, 1)`
	- Can use pattern matching to deconstruct it:
	```
	let tup: (u16, f32, u8) = (5, 5.7, 1);
	let (x, y, z) = tup;
	```
	- Each tuple element can be accessed using its index 
	```
	let a = tup.0;
	let b = tup.1;
	let c = tup.2;
	```
- Array: Every element in the array must have the same type and the array must be of fixed length
	- Ex: `let arr: [u8; 5] = [1, 2, 3, 4, 5]` - specify type and length
	- Initialize with same value: `let a = [3; 5]`
	- Access elements with `arr[<index>]`

### Functions
Rust convention is to use snakecase for function and variable names. 
```
fn sample_values(){
	// code
}
```
Functions must have their parameters type annotated: 
```
fn do_something(val: i32){
	// code
}
```
The type of the return value must be specified using `->`:
```
fn do_something() -> i32{

	return 10; 
}
```
A function will return the last expression implicitly if no return is specified. 

# Libraries
https://github.com/TheAlgorithms/Rust
https://github.com/tensorflow/rust
