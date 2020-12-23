# Parsing Trees

Parse trees are how the compiler breaks down what it needs to do. Understand that the tree goes left to right, bottom to top. Parse trees are a visual way of seeing precedence levels. When writing by hand, parse tree order can be seen with the parentheses around the different expressions, similar to regular arithmetic. Precendence can be set for different expressions. The higher the precendence level, the sooner it is executed, because the higher the precedence, the further down in the tree it is. We know that the tree goes bottom to top. 

Using the site for BNFC, we are given the grammar for a calculator:
```
EAdd. Exp  ::= Exp  "+" Exp1 ;
ESub. Exp  ::= Exp  "-" Exp1 ;
EMul. Exp1 ::= Exp1 "*" Exp2 ;
EDiv. Exp1 ::= Exp1 "/" Exp2 ;
EInt. Exp2 ::= Integer ;

coercions Exp 2 ;
```
We can see that the precendence levels for division and multiplication have a precendence level of 1, and addition and subtraction have a precendence level of 0. By default then, division and multiplication would be executed before addition and subtraction.
