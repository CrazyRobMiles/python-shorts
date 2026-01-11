# Tuple of One

We’ve seen that we can create a tuple by using brackets to “squish” things together:
```
x = ("Rob",21)
```
Tuples are very useful if you want to return multiple values from a function:
```
return ("Rob",21)
```
This lets me return name and age values. However, sometimes you might want to return just one item in a tuple. You might think you do this:

x = (1)

However, this doesn’t work. Python thinks that the brackets are part of an expression, gets rid of them and puts the value 1 in x. If you want to make it clear to Python that you are making a tuple, put a “spare” comma on the end:

x = (1,)

This would “tupleise” the value.

[Lists](/pages/05%20Lists.md)

[home](/README.md)