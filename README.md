matlab-parser
=============

ANTLRv4 parser for MATLAB programming language.

The front-end parser converts MATLAB source code to an parse tree / concrete syntax tree representation. The ANTLRv4 grammar does not contain any parser actions. The parse tree is subsequently processed by a series of tree node visitor which converts the concrete syntax tree to an abstract syntax tree (AST) and control flow graph (CFG).

