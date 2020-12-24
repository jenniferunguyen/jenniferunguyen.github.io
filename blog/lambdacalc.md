# Step 4: Lambda Calculus

Lambda calculus consists of 3 types of expressions. 
```
x 
E1 E2
\x.E
```
First, an expression, E, is made up of variables. Second. two expressions next to each other means that the first expression takes the second expression as input (known as application). Third, to define what the expression does, use a \ before the variable that the expression fill the input as then a period (this syntax will be used just because it is easier to write it this way). The E after the \. is the code on what the expression does (known as abstraction). An example would be 
```
(\x. x) 8
```
The result would be 8.

For lambda calculus, there exists a theorem called the [Church-Rosser theorem](https://www.youtube.com/watch?v=ROlXgCDA8ys). One of the biggest advantages of lambda calculus is the way abstraction works, because you can evaluate the function in any order (say one funciton on another, or the right one before the left one, or the left before the right) and still get the same answer. This makes it interesting to reduce lambda calculus expressions because you know that there are multiple ways to reduce it to the normal form. Added to the fact that the expression x can be anything, from a variable to lines of code. Let's see a simple case. We have the following:
```
(\x. x) (4 * 2)
```
One way to reduce is call by name, where you do application and replace the variable in the function with inputs. 
```
(\x. x) (4 * 2)
(4 * 2)
8
```
Another way is to do call by value, where you evaluate the argument first.
```
(\x. x) (4 * 2)
(\x. x) 8
8
```
In both ways, the final reduction goes to 8.

For a fun read, check out Aaron Christianson's post [here](https://www.quora.com/What-are-the-advantages-of-programming-languages-based-on-lambda-calculus).

Parentheses and spaces between letters are also very important to lambda calculus, because it defines the parse tree for the execution. `(\x. x) x y` returns `x` while `(\x. x) xy` returns `xy`.

Let's work through an example of reducing lambda calculus. 


Useful links:

[What is Lambda Calculus](https://www.jrebel.com/blog/what-is-lambda-calculus)

[Lambda Calculus](https://crypto.stanford.edu/~blynn/lambda/)
