# Step 2: Pattern Matching

Haskel uses recursion through a feature called pattern matching. To sucessfully write pattern matching, you have to break down what you want to do by the simplest cases of each computation step. This can be very frustrating to do, because it is thinking about a function in a way that you haven't before.

## Thinking Through Subtraction
We will use the subtraction example from the previuos post. To make it easier, we predefine numbers as O for 0 and S as how many from 0 the number is. Therefore, S S S O would be 3. We will only be using natural numbers in our scenario, just for simplicity. When thinking about subtraction, you take the larger number and remove the smaller number from it. This means that you make the larger number smaller, or closer to 0. In other words, you take the amount of steps equal to the smaller number from the larger number towards 0. 

That establishes the base of what we want our function to accomplish. I have found that it is easier to start with small examples. First most, we have to follow Haskell syntax since we are using natural numbers. The first line of our function would be 
```
subtr :: NN -> NN -> NN
```
which means that the function subtr take one natural number and evaluate it on another and then returns a natural number.

Now, we know that anything subtracted by 0 is just that number. Our secound line for our function would then be:
```
subtr n O = n
```
We have decided with this line of code that the larger number is the first number. To make sure that mistakes don't cause errors, we add 
```
subtr O n = O
```
so that the user can't subtract from 0, or subtracting from 0 would just be 0.

These are our base cases, meaning that we know each time we use this function, we want to get to these basic, simple cases. How can we think of subtraction in a way that brings us to one number being 0? Thinking of subtraction as steps towards 0, after each step, the larger number has one fewer step to take to get to 0. We already said that the number of steps should equal the smaller number. After each step then, the smaller number is also one less. Think about this as 5 - 4 = 4 - 3 = 3 - 2 = 2 - 1 = 1 - 0. We can write this as 
```
subtr (S n) (S m) = subtr n m
```
Haskell has pattern matching, meaning that it sees if the expression matches this pattern, if it does then the expression is evaluated following the code. Here is our whole function:
```
subtr :: NN -> NN -> NN
subtr n O = n
subtr O n = O
subtr (S n) (S m) = subtr n m
```

If we were to type in the terminal after loading the file containing our function
```
>subtr (S S S O) (S S O)
```
Haskell would recognized that this matches our fourth line of code, and return `subtr (S S O) (S O)`. Following these patterns, the next computation results in `subtr (S O) (O)` which matches our second line of code. The final result if S O. 

Yes, this breaking down of functions is confusing, but it lets you think about functions in a new way that really allows you to understand what you are doing. If you were to look at subtraction in C++,
```
subtr(x,y){return x-y}
```
You didn't have to run through the same thought process.

Haskell also has boolean values. 
```
less :: NN -> NN -> Bool
less n O = False
less O n = True
less (S n) (S m) = less n m
``` 
and lists
```
append [] ys = ys
append (x:xs) (ys) = x:(append xs ys)
```

Some syntax to know for writing in Haskell: you do not need to add a semicolon after each line like in C++, and to add a comment, just start the line with "--", double dashes.

