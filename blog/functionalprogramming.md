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
As you can see, imperative programming gives you the ability to explicitly assign values to variables. In functional programming, you do not have the ability to create an instances where you can manually update its value. Instead, you have to think of a recursive way to execute the same action. This brings up one of the benefits of functional programming: your code can be significantly shorter than in imperative programming. 
### Useful Link:
[Practical Differences Between Functional and Imperative Programming](https://sookocheff.com/post/fp/differences-between-imperative-and-functional/)

[7 Unbeatable Advantages of Functional Programming](https://medium.com/@devisha.singh/7-unbeatable-advantages-of-functional-programming-b5d1af1edbe1)

## Intro to Haskell
Haskell is the main functional programming language of this blog. Switching from imperative programming to functional programmin takes some time, because it requires one to think of the basis of a function. 

