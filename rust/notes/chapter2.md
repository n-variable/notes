# Setting Up a New Project
    $ cargo new <project-name>
    $ cd <project-name>

- Cargo new creates a new directory under the name of the argument and then populates the new directory with a <code>Cargo.toml</code> file (a standard similar to the <code>package.json</code> files of the npm package manager for node.js)

# Guessing Game
    use std::io;

    fn main() {
        println!("Guess the number?");
        println!("Please input a number: ");
        
        let mut guess = String::new();

        io::stdin()
            .read_line(&mut guess)
            .expect("Failed to read line");

        println!("You guessed: {}", guess);
    }
Source

## Breakdown
- Line 1: <code>use std::io</code> - Brings the <code>io</code> (input / output) library from the <code>std</code> library into scope (makes classes and methods from the library accesible in the project file).
- Line 2: <code> fn main() {</code> - Function declaration for function <code>main</code>
- Line 3: <code> println!("Guess the number?");</code> - Method call to println! macro (function calls with an exclamation at the end are macros rather than regular functions) which displays the argument in the console  / terminal.
- Line 4: <code> let mut guess = String::new();</code> - This line declares a new mutable reference variable <code>guess</code> that is initialized with an empty <code>String</code> object. The <code>mut</code> keyword ensures that this variable is not final and can be changed at a point in time after its declaration. the <code>=</code> operator ensures that the value of the out put of the method <code>String::new()</code> is bound to the reference variable <code>guess</code>.
- Line 5: <code>io::stdin().read_line(&mut guess).expect("Failed to read line");</code> - This line calls the <code>stdin()</code> method from the <code>io</code> library in the <code>std</code> library that we brought into scope earlier. We then call the <code>read_line()</code> method on the object returned by the <code>stdin()</code> method, passing in a reference to the mutable <code>guess</code> variable. The read_line() method seems to read some command line input and binds that value to the memory addressed passed into it. The <code>expect()</code> method is an exception handling method.
- Line 6: <code>println!("You guessed: {}", guess)</code> - This line uses the <code>println!</code> macro again in order to print a message to the console / terminal. The <code>{}</code> brackets indicate where to  insert the variable guess into the string before printing to console.

# Introduction to Crates
-  Rust crates are a collection of Rust source code files
-  Crates can be both *binary* and *library* crates.
-  Binary crates are executables which are meant to be run standalone, library crates are collections of Rust source code which are meant to be used by other programs.

# Using Crates
- When using someone elses crate as a dependency, simply add the dependency to your <code>Cargo.toml</code> file under the <code>[dependencies]</code> header
- Crates are