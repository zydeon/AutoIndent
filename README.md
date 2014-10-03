# qccompiler

Design and implementation of a compiler from scratch, including:
1. Lexical analysis
2. Syntactic analysis
..1. Abstract syntax tree (AST) construction
3. Semantic analysis
4. Code generation

It's written in C and it compiles input files written in qC, a small subset of the language ANSI C (C89/C90). The generated code is in C, but very close to Assembly.

## Features of qC
* use variables and literals of types *character* and *integer* (both with signal)
* pointers to variables and literals and to other pointers
* unidimensional arrays for integers, characters or pointers
* literals of type *string*
* arithmetic and logic expressions (check language grammar)
* simple relational operations
* pointer operations
* assign operations
* control operations (*if-else* and *while*)
* output operations (simplified version of *printf*)
* conversion between integers and strings - operations *itoa* and *atoi*
* comments of type /\* ... \*/

## Grammar

## Dependencies
* flex
* yacc
* gcc

## Usage

```
$ make
$ ./qccompiler [OPTIONS] < input.qc
```

OPTIONS

	-t	print the abstract syntax tree and stop after syntatic analisys.
	-s	print the symbol table and stop after semantic analisys.
	-c	allways compile the program (unless errors occur)
	-o	allways compile the program (unless errors occur) and print compiled program to file
		If both flags s and t are set, the proccess stops after the semantic analysis
		The result of the compilation is written to the file *result.c*

