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
- Line 4: <code> let mut guess = String::new();</code> - This line declares a new mutable reference variable <code>guess</code> that is initialized with an empty <code>String</code> object.
- Line 5: <code>io::stdin().read_line(&mut guess).expect("Failed to read line");