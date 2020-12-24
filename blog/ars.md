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
orange yellow blue red blue
orange green red blue
orange green purple
```
From our set of rules, we are not reaching the same answer. We want to then find a way to expand/modify our rules so that we do get a normal form. In order to do that, we need to make sure that before the colors are combined (seen when two colors reduce to one), the order of the colors will always be a specific way. In our example, we have two red, two yellow, and two blue. Say our goal of a normal form is to have the final reduction go to `red orange green blue`.  
