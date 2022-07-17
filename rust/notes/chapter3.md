# Chapter 3: Common Programming Concepts

## 3.1: Variables and mutability
### Variables
- Variables are denoted by the keyword <code>let</code>, and are immutable by default
- The keyword <code>mut</code> allows for mutable variables

### Constants
- Constants are permanently immutable values that can only be set at compile time (i.e. methods cannot set the values for a constant at run-time)
- Constants are denoted by the following notation: <code>const constName: 37 * 42</code>

### Variable Shadowing
- Variable shadowing is the practice of redeclaring a variable in order to override a previous variable state
- Allows immutable variables to be "updated" in a sense without being mutable at runtime

## 3.2: Data Types
- Rust is statically typed

### Scalar Types
- Scalar types represent single values

- Types
  - Integers
    - Number without fractional component
    - Integers can be both signed and unsigned (all integers vs natural numbers)
    - Integer types are denoted by <code>isize</code> for signed integers and <code>usize</code> for unsigned integers where <code>size</code> is the amount of space objects of the type will take up. (8, 16, 32, 64, 128)
    - The <code>size</code> of the integer type you use depends on system architecture e.g. 32-bit systems accept u32 or i32 type integers and 64-bit systems accept u64 or i64 type integers.
  - Floating Point Numbers
    - Floating point numbers  are decimals
    - Two possible types, <code>f32</code> and <code>f64</code> for 32-bit and 64-bit architectures
  - Boolean
    - Standard boolean stuff
  - Characters
    - Standard character stuff

### Compound types
- Compound types group multiple values into a single type
  
- Tuples
  - A general way of grouping a set of objects of arbitrary types
  - Fixed length structures
  - Syntax: <code>let tup: (u32, f32, u8) = (500, 6.4, 1)</code>

- Arrays
  - An ordered grouping of objects of arbitrary types
  - Fixed length structures
  - Implicit Syntax: <code>let a = [1, 2, 3, 4];</code>
  - Explicit Syntax: <code>let a: [i32, 5] = [1, 2, 3, 4, 5];</code>

## 3.3 Functions

- Void Function Declaration Syntax: <code>fn main(x : type, y : type) { ... }</code>
- Return Function Declaration Syntax: <code>fn main(x : type, y : type) -> type { ... }</code>

## 3.5 Control Flow

- IF Statements
  - General Syntax: <code>if condition { ... } else if condition { ... } else { ... }</code>
  - Inline Syntax (Ternary Operator): <code>let x = if condition { "string1" } else { "string2" }</code>

- Loop
  - <code>Loop</code> keyword tells Rust to execute a block of code forever (similar to while(True) { ... } in other languages).
  - Syntax: <code>loop { ... }</code>
  - <code>loop</code> can be used when a specific block of code must be tried until it executes
  - Returning values: <code>let x = loop { ... }</code>
    - Loops return the <code>break</code> value
  - Loops can be labeled
    - Syntax: <code>'loop_name': loop { ... }</code>
- While
  - Standard while loop stuff
    - Syntax: <code>while condition { ... }</code>
- For
  - For-Each Loops
    - Syntax: <code>for x in a { ... }</code>
  - Ranged For Loops
    - Syntax: <code>for x in (0..n).rev() { ... }</code>