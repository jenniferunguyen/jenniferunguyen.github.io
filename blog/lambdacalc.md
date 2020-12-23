# Step 4 Lambda Calculus

Lambda calculus consists of 3 types of expressions. 
```
E :: = x 
E1 E2
\x.E
```
E signifies an expression. First, an expression is made up of variables. Second. two expressions next to each other means that the first expression takes the second expression as input (known as application. Third, to define what the expression does, use a \ before the variable that the expression fill the input as then a period (this syntax will be used just because it is easier to write it this way). The E after the \. is the code on what the expression does (known as abstraction). An example would be 
```
(\x. x) 8
```
The result would be 8.

Useful link:
[What is Lambda Calculus](https://www.jrebel.com/blog/what-is-lambda-calculus)
