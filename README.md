# jlox - Java Lox Interpreter

A Java implementation of the **Lox** programming language, following the book [*Crafting Interpreters*](https://craftinginterpreters.com/) by Robert Nystrom.

## 📂 Project Structure
The source code is organized inside the `src` directory following standard Java package structure:
```text
src/
 └── com/
      └── craftinginterpreters/
           ├── lox/
           │    ├── Expr.java         # (New) Auto-generated AST classes
           │    ├── Lox.java          # Main entry point
           │    ├── Scanner.java      # Tokenizer
           │    ├── Token.java        # Token definitions
           │    ├── TokenType.java    # Enum of token types
           │    ├── AstPrinter.java
           │    ├── Stmt.java
           │    ├── RuntimeError.java
           │    └── Parser.java
           │
           └── tool/                  # (New) Build tools
                └── GenerateAst.java  # Script to generate Expr.java
````

## 🚀 How to Build & Run

**Prerequisite:** Ensure you have Java (JDK) installed.

### 1\. Compilation

Navigate to the `src` folder and compile the package:

```bash
cd src
javac com/craftinginterpreters/lox/*.java
```

### 2\. Running the REPL

To start the interactive prompt (Read-Eval-Print Loop), run the main class without arguments:

```bash
java com.craftinginterpreters.lox.Lox
```

*Type Lox code (e.g., `print "hello";`) and press Enter to see the tokens.*

### 3\. Running a Script

To run a specific `.lox` file:

```bash
java com.craftinginterpreters.lox.Lox path/to/script.lox
```

## ✅ Current Progress

  - [x] **Scanning (Lexical Analysis)**: Converts source code into tokens.
  - [x] **Parsing**: Turns tokens into an Abstract Syntax Tree (AST).
  - [ ] **Static Analysis**: Variable resolution and type checking.
  - [ ] **Interpreting**: Executing the AST.

## 📝 Example Code

```lox
var language = "Lox";
print "Hello, " + language;
```
