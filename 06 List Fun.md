# 06 List Fun

Python lists are nice. We can make them very easily:
```
x = [1,2,3]
```
The order of the list is preserved. If we work our way through the elements they will always come out in the same order. We can use the len function to find out how many things are in a list:
```
l = len(x)
```
If we want to add something to a list we can use the append behaviour provided by lists:
```
x.append(5)
```
This will pop 5 on the end of the list. There’s no “prepend” function for putting something at the start of a list. Instead there’s an insert function that can be used to insert something at a particular position:
```
x.insert(0,0)
```
This statement would put the value 0 at the start of list x. You can use the remove behaviour to get rid of an element at a particular position in the list and pop, which removes an item and returns it. 

[Dictionaries](/07%20Dictionaries.md)

[home](/README.md)