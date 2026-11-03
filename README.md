# 🦀 Rust Programming Language

## Introduction
Rust is a systems programming language focused on performance, memory safety, and concurrency without requiring a garbage collector.

## Variables
```rust
fn main() {
    let name = "Utkarsh";
    let mut age = 22;
    age = 23;

    const PI: f64 = 3.14;
}
```

## Data Types
- Integer: `i32`, `i64`, `u32`
- Float: `f32`, `f64`
- Boolean: `bool`
- Character: `char`
- String: `String`, `&str`
- Tuple
- Array
- Vector

## Functions
```rust
fn add(a: i32, b: i32) -> i32 {
    a + b
}

fn main() {
    println!("{}", add(10, 20));
}
```

## Conditions
```rust
let age = 20;

if age >= 18 {
    println!("Adult");
} else {
    println!("Minor");
}
```

## Loops
```rust
for i in 0..5 {
    println!("{}", i);
}

let mut count = 0;

while count < 5 {
    println!("{}", count);
    count += 1;
}
```

## Arrays and Vectors
```rust
let arr = [10, 20, 30];

let mut nums = vec![1, 2, 3];
nums.push(4);
```

## Structs
```rust
struct User {
    name: String,
    age: u32,
}

fn main() {
    let user = User {
        name: String::from("Utkarsh"),
        age: 22,
    };
}
```

## Ownership and Borrowing
Rust uses ownership rules to ensure memory safety.

```rust
let name = String::from("Rust");

let borrowed = &name;      // Immutable borrow
let mutable = &mut String::from("Hello"); // Mutable borrow
```

## Pattern Matching
```rust
let number = 2;

match number {
    1 => println!("One"),
    2 => println!("Two"),
    _ => println!("Other"),
}
```

## Error Handling
```rust
fn divide(a: f64, b: f64) -> Result<f64, String> {
    if b == 0.0 {
        Err(String::from("Division by zero"))
    } else {
        Ok(a / b)
    }
}
```

## Important Concepts
- Ownership
- Borrowing
- References
- Lifetimes
- Structs and Enums
- Pattern Matching
- Traits
- Generics
- Option and Result
- Cargo and Crates
- Concurrency
- Smart Pointers

## Useful Resources
- [Official Rust Documentation](https://doc.rust-lang.org/book/)
- [Rust By Example](https://doc.rust-lang.org/rust-by-example/)
- [Rust Playground](https://play.rust-lang.org/)

---

**Happy Coding! 🦀**
