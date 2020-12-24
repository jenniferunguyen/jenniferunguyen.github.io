# Step 7: Measure Functions

We have discussed the concept of finding a normal form, or end result, from an ARS. How do we know that we have reached the normal form? How do we show termination, an end to the computations? Like an invariant, a measure function is something that we can find that helps us. In a measure function, the basic premise is that the measure function used on a later step would have a smaller value than on an earlier step. We can use our ARS from before that is defined by the rules:
```
red red red -> red 
red red ->
```
How do we know that 5 red really ends at 1 red? Our measure function can be defined as the number of reds. We start off with 5 reds, which can be reduced to 3 reds, then 1 red. 1 is less than 5, so our measure function has shown that the ARS terminate. Simplying counting the number of reds is not an official measure function. A more formal measure function would be to assign each red as the value of 1, and adding the total values of the string. 

In many cases, assigning the elements of the string to a number is a simple way to create a measure function. It becomes very easy to compare natural numbers. This is not always the case, unfortunately. For some programs, it may not be possible to assign numbers and use arithmetic to total a value for the step.  
