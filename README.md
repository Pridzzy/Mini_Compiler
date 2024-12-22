# C Source to Assembly Code Compilation Workflow

This project provides a workflow for compiling a C source file (`source.c`) into assembly code (`assembly.s`). The process involves the following steps:

1. **Lexical Analysis** (using `lex.l`): Identifies tokens in the source code.
2. **Parsing** (using `yacc.y`): Defines grammar and syntax rules, generating a parser.
3. **Intermediate Code Generation and Optimization**: Produces an intermediate file (`intermediate.i`) with optimized 3-address code.
4. **Assembly Code Generation**: Produces the final assembly code in the `assembly.s` file.

## Files

- **lex.l**: Lexical analyzer code written in Lex, which defines tokens for the source code.
- **yacc.y**: Parser code written in Yacc, which defines grammar and syntax rules to generate a parser.
- **source.c**: The input C source file that will be compiled to produce intermediate and assembly code.
- **intermediate.i**: The output file containing the optimized 3-address intermediate code.
- **assembly.s**: The output file containing the generated assembly code.
- **build.sh**: A shell script that automates the process of building intermediate and assembly code.

## Prerequisites

Ensure you have the following tools installed:

- **Lex**: A lexical analyzer generator.
- **Yacc**: A parser generator.
- **GCC**: The GNU Compiler Collection for compiling the generated code.

## How to Run

1. Place all the files (`lex.l`, `yacc.y`, `source.c`, and `build.sh`) in the same directory.
2. Open a terminal in that directory.
3. Run the following command to begin the build process:

   ```bash
   sh build.sh
