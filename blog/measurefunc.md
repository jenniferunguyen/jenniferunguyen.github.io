# Step 7: Measure Functions

We have discussed the concept of finding a normal form, or end result, from an ARS. How do we know that we have reached the normal form? How do we show termination, an end to the computations? Like an invariant, a measure function is something that we can find that helps us. In a measure function, the basic premise is that the measure function used on a later step would have a smaller value than on an earlier step. We can use our ARS from before that is defined by the rules:
```
red red red -> red 
red red ->
```
How do we know that 5 red really ends at 1 red? Our measure function can be defined as the number of reds. We start off with 5 reds, which can be reduced to 3 reds, then 1 red. 1 is less than 5, so our measure function has shown that the ARS terminate. Simplying counting the number of reds is not an official measure function. A more formal measure function would be to assign each red as the value of 1, and adding the total values of the string. 

In many cases, assigning the elements of the string to a number is a simple way to create a measure function. It becomes very easy to compare natural numbers. This is not always the case, unfortunately. For some programs, it may not be possible to assign numbers and use arithmetic to total a value for the step. Take for example a circular list. We have the follwoing rewrite rules:
```
red blue red -> red
```
Our circular list comtains the following elements `red red blue blue red blue` and repeats. Examining this looping string, we can reduce it to the elements of `red blue blue red`, but how do we prove that we are done for a circular list, when the length is not determinable. If we are not able to determine a measure function, we can resort to other ways to saying that a function has terminated. One possible thought is when the program returns the same value or output for after a step as before. We can then design an algorithm that recognizes when it is repeating the same iteration. This could be a potential solution. 

## The Halting Problem
This [video](https://www.youtube.com/watch?v=92WHN-pAFCs) explains the halting (think terminating) problem very well. Basically, it is impossible to create a way to determine if a program will halt or be stuck forever, by just taking in an input. In an imperative language like C++, it would be like designing an algorithm that tells us if we would get an infinite loop based on an input. This can not be accomplish and the only true way to know is the run the algorithm.
