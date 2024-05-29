# Simple Lightweight Instructional C Compiler (SLICC)

## Authors
Caleb L'Italien, John Daly, Kevin Welch, Thomas Breimer, Livi Gwinnett, Aaron Cass

## Overview
SLICC is a compiler for a subset of the C99 standard, designed for undergraduate-level compiler design courses. It utilizes LLVM for backend processing, with `SafeLLVM` serving as a wrapper for `llvm_sys`.

## Project Structure
- `common/`: Definitions for `AST` and shared modules.
- `integration/`: Integrates functionality from `common` and `sts` into `ir`.
- `ir/`: Converts instances of `Module` into pre-compiled LLVM modules.
- `lexer/`: Transforms source code into instances of `Token`.
- `parser/`: Constructs an `AST` from instances of `Token`.
- `src/`: Main driver for the compiler.
- `sts/`: Generates a `Symbol Table Stack (STS)` from an `AST`.
- `tests/`: Conducts end-to-end testing by processing a `.c` file through `src` and validating the resulting LLVM module.

## Features
- Includes a `Dockerfile` for each assignment, enabling completion without local installations.
- SafeLLVM provides a simplified and safe API for interfacing with LLVM.

## Getting Started
### Prerequisites
- Compatible with major Linux distributions and MacOS.
- `llvm-17`, `llvm-17-dev`, and `llvm-17-tools`
- `clang-17`
- `llvm_sys`
- `rustc`
- `cargo`

Alternatively:
- Docker CLI
- Docker Daemon

### Installation
Clone the repository and navigate to the project directory:
```
git clone git@github.com:UnionCompilerDesign/starter_code.git
cd starter_code
```
Build and test the project using Cargo:
```
cargo build --all
cargo test --all
```

### Usage
SLICC is freely available for use. A complete version of the project can be provided upon request by instructors.

### How to Contribute
Contributions are welcome! Please refer to the CONTRIBUTING.md file for guidelines on how to submit patches and bug reports. Contributions to the complete version are restricted to avoid potential conflicts of interest and breaches of academic integrity.

### License
Distributed under the MIT License. See the LICENSE file for more details.

### Acknowledgements
Special thanks to Professor Aaron Cass of Union College for his guidance and expertise throughout the development of this project.

### Contact
For any inquiries, contact Caleb L'Italien at litaliencaleb@gmail.com.

