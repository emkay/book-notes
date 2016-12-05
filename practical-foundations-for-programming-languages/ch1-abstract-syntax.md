# Abstract Syntax

* Programming langs express computations to both humans and machines
* syntax specifies how phrases combine to form programs
* what are these phrases? what is a program made of?

Informal concept of syntax:
* _surface_ or _concrete_ syntax concerned with _how_ phrases are entered and displayed on a computer. Strings of characters.
* _structural_ or _abstract_ syntax concerned with the structure of phrases, how they are composed from other phrases

Phrase is a tree: AST(Abstract Syntax Tree)
* nodes are operators that combine several phrases to form another phrase
* _binding_ structure of syntax concerned with the introduction and use of identifiers: how they are declared, how they can be used.

ABT(Abstract Binding Tree): enrich AST with concepts of binding and scope.

Not concerned with _concreate_ syntax.

"Pieces of syntax" are finite trees augmented with a way to express binding and scope.

Piece of syntax:
1. define AST, hierarchical structure of a piece of syntax
2. augment AST with binding(declaration) and scope(range of significance) of an identifier

This creates an ABT.

## 1.1 Abstract Syntax Trees

AST is an ordered tree where the leaves are _variables_ and the interior nodes are _operators_ where the _arguments_ are its children.

_variable_ stands for an unspecified or generic piece of syntax. an unknown place holder. meaning given by substitution.

_operators_ can combine ASTs

[_arity_](https://en.wikipedia.org/wiki/Arity) type and number of arguments of a function or operation

[_structural induction_](https://en.wikipedia.org/wiki/Structural_induction) priciple of reasoning. proof method used to prove that some proposition P(x) holds for all x of some sort.

## 1.2 Abstract Binding Trees

ABTs enrich ASTs with the means to introduce new variables and symbols called a _binding_, with a specified range of significance called a _scope_.

the scope of a binding is an ABT where the bound identifier can be used as a place holder (variable declaration) or as an index of some operator (symbol declaration).

the set of active identifiers can be larger within a subtree of an ABT than the surrounding tree.

crucial principle, any use of an identifier should be understood as a reference, or abstract pointer, to its binding.
