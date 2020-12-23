# Step 2: Pattern Matching

Haskel uses recursion through a feature called pattern matching. To sucessfully write pattern matching, you have to break down what you want to do by the simplest cases of each computation step. This can be very frustrating the do, because it is thinking about a function in a way that you haven't before.

## Recursion
We will use the subtraction example from the previuos post. To make it easier, we predefine numbers as O for 0 and S as how many from 0 the number is. Therefore, O S S S would be 3. We will only be using natural numbers in our scenario, just for simplicity. When thinking about subtraction, you take the larger number and remove the smaller number from it. This means that you make the larger number smaller, or closer to 0. In other words, you take the amount of steps equal to the smaller number from the larger number towards 0. 

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
so that the user can't subtract from 0.

## Matching
