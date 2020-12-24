# Step 6: Invariants

Invariants can be used to determine the normal form of an ARS, so that it is not necessary to manually compute through each step of the ARS until a normal form is reached. By definition, an invariant is true before and after the computation step; an invariant doesn't vary. For example, say that our ARS only has two rules:
```
red red red -> red
red red ->
```
If we start with `red red red red`, we can write an invariant as (number of reds) mod 2. For each step of computation, this invariant holds true.
```
red red red red
red red

```
We have (number of reds) mod 2 = 0 for all steps. If we start with 'red red red red red red red', we compute the following:
```
red red red red red red red 
red red red red red 
red red red
red
```
We have (number of reds) mod 2 = 1 for all steps.

Invariants are properties that are always true. Using them to determine the normal form follows the understanding that the invariant must hold true for the normal form as well as what we started with. We know that our ARS reduces the number of red until it is no longer possible to reduce anymore, meaning there is only one red. We also know that the invariant on the (number of reds) mod 2 works. As you can see, we can predict the normal form using this invariant. Without working it out, we know that starting with 4 red, our normal form is 0 red. With an odd number of red, our normal form is 1 red.

Invariants are not limited to ARS. Invariants are can be seen with object oriented programming as well. They can be used to check the errors in instances of a class. Using an example from [Class Invariants](http://people.cs.aau.dk/~normark/oop-csharp/html/notes/contracts_themes-class-inv-sect.html), a class for a circular list can have an invariant where a list with at least one node would always be circular. Therefore, every instance made of the class has to have at least one node, otherwise it is not a circular list.

Invariants are used by the programmer to check their work. A compiler doesn't need to have invariants manually coded, because invariants are determined by the programmer based on relations that they have observed.
