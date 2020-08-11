# Pascal-Interpreter-flask
An elementary Interpreter for Pascal Programming Language developed in Python.

## Core Features
- **Tokenizer**
- **Parser** 
- **Semantic Analyser** 
- **Interpreter**


### Tokenizer
The Tokenizer, Lexical Analyser, is defined as a Class. It has methods that extract out RESERVED_KEYWORDS, variables and operators from the input code. The Tokenizer generates tokens as and when required by the Parser. In case an undefined stream of characters is witnessed, it throws an Exception.

### Parser
The Parser is governed by the pre-defined grammar for Pascal programming language. Based on the grammar rules, it parses out phrases from the code and generates nodes for the Abstract Syntax Tree (AST). The AST generated is used as an Intermediate Representation of the code snippet on which Semantic Analysis and Interpretation is done. The possible nodes that can be generated are pre-defined and code is converted into an AST by the Parser.

### Semantic Analyser
The Semantic Analyser is responsible for performing basic semantic analysis of the snippet and store varibles as Symbols in the Scoped Symbol Tables, inlcuding Procedure name variables. It checks if a varible has been defined prior to using it and if it belongs to the right scope. It does so by traversing the AST.

### Interpreter
The Interpreter maintains a Call Stack for Procedure/Function Calls, called Activation Records. Maintains the values of assigned variables and interprets the whole AST to give the final result.
