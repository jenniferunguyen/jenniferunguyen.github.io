# Step 5: Abstract Reduction Systems

Abstract reduction systems are also known as abstract rewriting system. They provide rules that we can use to rewrite a string. For example, say you have the following rules:
```
red yellow -> orange
yellow red -> red yellow
yellow blue -> green
blue yellow -> yellow blue
blue red -> red blue
red blue -> purple
```
Using these rules, we would reduce any part of a string that we have where a rule is applicable. Note that the order in which we use the rules does not matter, because an ARS is a group of rules, not an order of rules with precedence levels. An example follows. Of course, there are numerous ways to reduce the following.
```
blue red yellow yellow red blue
red blue yellow yellow red blue
purple yellow yellow red blue
purple yellow yellow purple
```
or
```
blue red yellow yellow red blue
red blue yellow yellow red blue
red yellow blue yellow red blue
red yellow yellow blue red blue
red yellow yellow red blue blue
red yellow red yellow blue blue
red red yellow yellow blue blue
red orange yellow blue blue
red orange green blue
```
In the first reduction, we reduce from two colors to one as soon as we could. In our second reduction, we focused on the order before combining colors. From our set of rules, we are not reaching the same answer. Say that we want to then find a way to expand/modify our rules so that we do get one normal form. In order to do that, we need to make sure that before the colors are combined (seen when two colors reduce to one), the order of the colors will always be a specific way. In our example, we have two red, two yellow, and two blue.  

If we were to remove the reordering rules, so that our ARS is just
```
red yellow -> orange
yellow blue -> green
red blue -> purple
```
In this case, the order can not be rewritten. An example reduction would then be
```
blue red yellow yellow red blue
blue orange yellow red blue
blue orange yellow purple
```
Now, we have obtained a normal form.
