# Variables

## Binding and mutability

1. 🌟 A variable can be used only if it has been initialized.

```rust
// Fix the error below with least amount of modification to the code
fn main() {
    let x: i32 = 5; // Uninitialized but used, ERROR !
    let y: i32; // Uninitialized but also unused, only a Warning !

    assert_eq!(x, 5);
    println!("Success!");
}
```

2. 🌟 Use mut to mark a variable as mutable.

```rust
// Fill the blanks in the code to make it compile
fn main() {
    let mut x : i32 = 1;
    x += 2; 
    
    assert_eq!(x, 3);
    println!("Success!");
}
```

## Scope

A scope is the range within the program for which the item is valid.

```rs
// Fix the error below with least amount of modification
fn main() {
    let x: i32 = 10;
    {
        let y: i32 = 5;
        println!("The value of x is {} and value of y is {}", x, y);
        println!("The value of x is {} and value of y is {}", x, y); 
    }
}
```

```rs

// Fix the error with the use of define_x
fn main() {
    define_x();
    
}

fn define_x() {
    let x:&str = "hello";
    println!("{}, world", x); 
}
```

## Shadowing

You can declare a new variable with the same name as a previous variable, here we can say the first one is shadowed by the second one.

```rs
// Only modify `assert_eq!` to make the `println!` work(print `42` in terminal)
fn main() {
    let x: i32 = 5;
    {
        let x = 12;
        assert_eq!(x, 12);
    }

    assert_eq!(x, 5);

    let x = 42;
    println!("{}", x); // Prints "42".
}
```

```rs
// Remove a line in the code to make it compile
fn main() {
    let mut x: i32 = 1;
    x = 7;
    // Shadowing and re-binding
    // let x = x;  Remove this
    x += 3;


    let y = 4;
    // Shadowing
    let y = "I can also be bound to text!"; 

    println!("Success!");
}
```

```rs
// Fix the error below with least amount of modification
fn main() {
    // let (x, y) = (1, 2);
    let (mut x, y) = (1, 2);
    x += 2;

    assert_eq!(x, 3);
    assert_eq!(y, 2);

    println!("Success!");
}
```

```rs
fn main() {
    let (x, y);
    (x,..) = (3, 4);
    [.., y] = [1, 2];
    // Fill the blank to make the code work
    assert_eq!([x,y], __);
    // assert_eq!([x,y], [3,2]); Solution

    println!("Success!");
} 
```
