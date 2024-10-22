# My Parser

### This is a simple parser that uses PEG macros to parse lists of numbers.

## Description
### This crate allows parsing a string representation of a list of unsigned integers (u32), separated by commas, into a vector. For example, the string "[1,1,2,3,5,8]" will be successfully parsed into a Vec<u32> containing the corresponding values.

## Usage Example

```rust
use my_test_parser_krylchuk::list_parser;

fn main() {
    // Parsing a list of numbers
    let parsed_data = list_parser::list("[1,1,2,3,5,8]");
    println!("{:?}", parsed_data);

    // Verifying the parsing result
    assert_eq!(
        list_parser::list("[1,1,2,3,5,8]"),
        Ok(vec![1, 1, 2, 3, 5, 8])
    );
}
```

## Installation
### Add this to your Cargo.toml:

```rust
[dependencies]
my_test_parser_krylchuk = "0.1.0"
```

## License
### This project is licensed under the MIT License.