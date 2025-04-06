# 💻 Compiler Design Project – MACC Instruction Parser

## 📚 Project Description

This project is a simple compiler front-end built using **Flex (Lex)** and **Bison (Yacc)** as part of a Compiler Design course or lab. The main goal is to demonstrate how high-level expressions can be tokenized, parsed, and translated into a custom intermediate representation.

### 🧾 What It Does

The program takes an arithmetic expression in the following fixed format:

result = a * b + c * d;

```vbnet

And converts it into a custom **MACC (Multiply and Accumulate)** instruction:
```
macc result, a, b, c, d

```pgsql


### 🎯 Key Concepts Demonstrated

- **Lexical Analysis**: Tokenizing identifiers, numbers, and symbols using Flex.
- **Syntax Analysis**: Parsing specific grammar rules with Bison.
- **Intermediate Code Generation**: Producing a single-line custom instruction (`macc`).

This is a minimal but effective example of how compilers transform input code into lower-level  representations. It focuses on a specific grammar pattern and is easy to extend to support more complex parsing tasks.
```

```
## ⚙️ Build Instructions

Follow the steps below to compile and run the project. Ensure you have **Flex**, **Bison**, and **GCC** installed on your system.

---

### 🛠️ Compile the Lexer and Parser

Run the following commands in your terminal:

```bash
bison -d parser.y       # Generates parser.tab.c and parser.tab.h
flex lexer.l            # Generates lex.yy.c
gcc parser.tab.c lex.yy.c -o macc_parser  # Compiles everything into an executable
```
This will produce an output file called macc_parser.

▶️ Run the Program
To execute the parser:

```bash
./macc_parser
```
Then type the expression you want to parse, for example:

```ini

result = a * b + c * d;
```
Press Enter, and you'll get:

```less
Custom instruction: macc result, a, b, c, d
```
