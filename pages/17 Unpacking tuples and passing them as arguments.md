# Unpacking tuples and passing them as arguments

Tuples are a great way to group data together. Say I want to pass into a function the minimum and maximum values for a particular random item. Say I was writing a function to draw stars, and I want to make random ones with points in the range 5 to 20. I can make tuple like this to express the requirement.
```python
points_min_max=(5,20)
```
This makes me a tuple with the two values. However, when I call **random.randint** from the random library it wants two individual arguments. I could do this by getting each value out of the tuple and passing it into the call:
```python
random.randint(points_min_max[0],points_min_max[1])
```
This is not very elegant, and it would be a real pain if I wanted to pass lots of tuple values. So, instead Python lets you do this:
```python
random.randint(*points_min_max)
```
We just have to specify the name of the tuple variable, preceded by a * which in this context means "unpack". When the function or method is called Python will convert the values in the tuples into individual arguments and then pass those. The order of the arguments matches the order of the values in the tuple. 


[home](/README.md)