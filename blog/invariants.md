# Step 6: Invariants

Invariants can be used to determine the normal form of an ARS, so that it is not necessary to manually compute through each step of the ARS until a normal form is reached. By definition, an invariant is true before and after the computation step. For example, say that our ARS only has one rule:
```
red red red -> red
```
If we start with `red red red red`, we can write an invariant as (number of reds) mod 2. For each step of computation, this invariant holds true.
```
red red red red
red red
```
We have (number of reds) mod 2 = 0 for both steps. If we start with 'red red red red red red red', we compute the following:
```
red red red red red red red 
red red red red red 
red red red
red
```
We have (number of reds) mod 2 = 1 for all steps
