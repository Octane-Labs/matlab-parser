matlab-parser
=============

ANTLRv4 parser for MATLAB programming language.

Project Description
-------------
MATLAB is a high performance language geared toward technical computing. The language provides powerful features that among other things, enable matrices and arrays to be efficiently and easily manipulated. These features are also high level and this makes the usage of the language very intuitive. 

MATLAB syntax analysis is quite challenging. Examples include tackling the single quote character, efficiently building uniform colon expressions and handling matrix constructs.

We began by adapting the grammar from GNU Octave, a language inspired by MATLAB and sharing much of MATLAB’s syntactic and semantic features. From Octave, a core set of grammar productions were retained and modified and many more added to capture MATLAB’s syntax as faithfully as possible.

The front-end parser converts MATLAB source code to an parse tree / concrete syntax tree representation. The ANTLRv4 grammar does not contain any parser actions. The parse tree is subsequently processed by a series of tree node visitor which converts the concrete syntax tree to an abstract syntax tree (AST) and control flow graph (CFG).

Features
-------------
The parser currently supports only a proper subset of the MATLAB language. The current version recognizes:
- script and function .m files,
- expressions,
- assignments,
- if statements,
- for loops,
- while loops,
- return statements,
- global declarations,
- a limited form of the _command form_ of function invocations

Limitations
-------------
Support is presently unavailable for:
- switch statements,
- structures,
- cell arrays
