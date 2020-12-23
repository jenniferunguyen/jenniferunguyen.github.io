# Step 1: Functional Programming

## What is Functional Programming
Functional programming is a very different method of programming than the traditional, imperative programming that one thinks of. 

In imperative programming, each line of code tells the computer exactly what to do. This makes programming very procedural, because the programmer focus on what they need the code to do and write to achieve those actions. Common languages of imperative programming are C++ and Java. 

For functional programming, lines of code explain how something is, rather than what it does. Everything is an expression, meaning that everything evaluates to something. Haskell will be the language used in this blog. 

These short descriptions may be confusing, so I found an analogy on a Stack Overflow [post](https://stackoverflow.com/questions/17826380/what-is-difference-between-functional-and-imperative-programming-languages). The response details how you would think of imperative programming versus functional programming. For example, in imperative programming, you would have a designated set of actions, such as grabbing your keys, openning your garage door, and starting your car. In functional programming, the idea of how things works is what you would have: keys are used to unlock things, car are made as a mode of transportation, and the garage is a storage unit. 

Because of how different functional programming works than imperative programming, the way you write code is different. In imperative programming, the programmer is used to explicitly writing how something works. For example, in C++ to show addition of two numbers, you can write
```
int x = 1;
int y = 2;
y = x + y;
```
As you can see, imperative programming gives you the ability to explicitly assign values to variables. In functional programming, you do not have the ability to create an instance or variable where you can manually update its value. Variables are fixed at what they are initialized at. Instead, you have to think of a recursive way to execute the same action. This brings up one of the benefits of functional programming: your code can be significantly shorter than in imperative programming, because your code is reusable. 

Another advantage to functional programming is its use of "lazy evaluation." Lazy evaluation is a compiler not evluating an expression until it needs to. For example, if a function is to take the first argument as x and add 2, but the function takes in two parameters x and y. The user can input anything for y, say 5-3, and in this case, the compiler would never evaluate 5-3, because it doesn't need to.
### Useful Links:
[Practical Differences Between Functional and Imperative Programming](https://sookocheff.com/post/fp/differences-between-imperative-and-functional/)

[7 Unbeatable Advantages of Functional Programming](https://medium.com/@devisha.singh/7-unbeatable-advantages-of-functional-programming-b5d1af1edbe1)

## Intro to Haskell
Haskell is the main functional programming language of this blog. Switching from imperative programming to functional programmin takes some time, because it requires one to think of the basis of a function and of course, there are some syntax difference (more on that in later posts). To start, use the `ghci` command in your terminal. 

Now, we get familiar with Haskell. In the terminal, you can enter a line and Haskell will evaluate it, because as mentioned above, everything is an expression. Try
```
>5*8
>10-9
>(7-3)*4
>7-3*4
```
Notice that in the last example, the multiplication is evaluated before the subtraction. This is because Haskell has preset precedence levels. These levels tells Haskell which functions to evaluate first. The levels can range from 0 to 9.

There is this amazing Haskell [cheat sheet](https://hackage.haskell.org/package/CheatSheet-1.7/src/CheatSheet.pdf) the provides a very nice guide to Haskell. I recommend skimming this for the new syntax and basic information. 

Now, you can define functions in the terminal of Haskell as well, though using a file is more usable for multiple-line functions. An example is subtraction.
```
>subtr x y = x - y
```
Here, we do not need to use any parantheses. We have defined a function called "subtr" that do subtraction for us. 
```
>subtr 7 3
4
```
If we were to use our function in the above example, we can see that our function subtr has a higher precedence level than the operator *.
```
>subtr 7 3 * 4
16
```

Here are a couple of useful commands to wrap up this introduction. 
`:load <FILENAME>.hs` allows you to open and use the functions in the file;
`:help` provides a list of commands;
`:quit` closes the interpreter, ghci.

