# jlox - Java Lox Interpreter

A Java implementation of the **Lox** programming language, following the book *[Crafting Interpreters](https://craftinginterpreters.com/)* by Robert Nystrom.

## 📂 Project Structure

The source code is organized inside the `src` directory following standard Java package structure:

```text
src/
 └── com/
     └── craftinginterpreters/
           ├── lox/
           │   ├── Lox.java           # Main entry point
           │   ├── Scanner.java       # Lexical analysis
           │   ├── Token.java         # Token data structure
           │   ├── TokenType.java     # Token type definitions
           │   ├── Expr.java          # (Generated) AST nodes for expressions
           │   ├── Stmt.java          # (Generated) AST nodes for statements
           │   ├── Parser.java        # Recursive descent parser
           │   ├── Interpreter.java   # The heart of the execution logic
           │   ├── Environment.java   # Handles variable bindings and scopes
           │   ├── RuntimeError.java  # Custom error handling
           │   └── AstPrinter.java    # Debug utility to visualize the AST
           │
           ├── lox_test_files/ test files to check how my jlox runs!
           └── tool/                  
               └── GenerateAst.java   # Tool to automate AST class creation

```

## 🚀 How to Build & Run

**Prerequisite:** Java JDK 8 or higher.

### 1. Compilation

Navigate to the `src` folder and compile the package:

```bash
cd src
javac com/craftinginterpreters/lox/*.java

```

### 2. Running

You can run a script file or enter the REPL:

```bash
# Run a file
java com.craftinginterpreters.lox.Lox path/to/script.lox

# Run the REPL
java com.craftinginterpreters.lox.Lox

```

## ✅ Roadmap (jlox)

* [x] **Ch 4: Scanning** - Lexical analysis and tokenization.
* [x] **Ch 5: Representing Code** - Defining the AST and the Visitor pattern.
* [x] **Ch 6: Parsing Expressions** - Recursive descent parsing.
* [x] **Ch 7: Evaluating Expressions** - Realizing the interpreter (math, logic).
* [x] **Ch 8: Statements and State** - Variables, print statements, and block scope.
* [ ] **Ch 9: Control Flow** - `if` statements and `while`/`for` loops.
* [ ] **Ch 10: Functions** - Function declarations, calls, and closures.
* [ ] **Ch 11: Resolving and Binding** - Semantic analysis (static scope).
* [ ] **Ch 12: Classes** - Instances, methods, and properties.
* [ ] **Ch 13: Inheritance** - Superclasses and method overriding.

## 📝 Example Scoping Test

```lox
var a = "global";
{
  var a = "local";
  print a; // local
}
print a; // global

```
