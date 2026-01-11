# Tuples vs Lists: Fight!

We can use tuples and list to make collections of data.

```python
red_tuple = (255,0.0)
red_list = [255,0,0]
```
The statements above make a tuple and a list that stores the colour red (all the red, no blue and no green) as three component values. 

Note that the choice of delimiter is what distinguishes a tuple from a list. Note also that since both of these can be iterated (worked through one at a time) we can use them interchangeably in lots of situations:

We can also use indexing to get values out of these collections:

```python
red_intensity = red_tuple[0]
```
This statement would get the red intensity from the value at the start of the red tuple. The same construction would work for **red_list**.

We can even use fancy unpacking these (I love this construction):

```python
(r,g,b) = red_list
```

This would pull out the component values of the red list and put them in the variables **r**, **g** and **b**. Note that if the list is not long enough (if we try to unpack a value which isn't there) we get an error:

```
(r,g,b,i)=red_list
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: not enough values to unpack (expected 4, got 3)
```

We can also iterate through tuples and lists:

```python
for component in red_tuple:
    print(component)
```


This would print the component values for either the tuple or the list version of the colour. 


So far, so lovely. But what what happens if we try to darken our red colour by decreasing the intensity of the red component?

```python
red_list[0]=128
```

This works fine because a list is implemented as a pointer to a memory locations that store the values in the list. But consider this: 

```
red_tuple[0]=128
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'tuple' object does not support item assignment
```

If I try to dim the red value in **red_tuple** it the operation fails. It turns out that tuples are  **immutable**. Immutable means "Once I've made this thing, you can't change what's in it". We can't change what's in **red_tuple** once it has been created. This might seem a bit strange. Why make something that can't be changed. Well, sometimes we don't want values to change. Consider this:

```Python
dot = red_list
```

I've made a variable called **dot** (which could part of a display). I want it to be bright red so I've is set to the value in **red_list**. But if I change the value of a component in  **red_list**, I'm effectively changing the value of **dot** as well. Which I might not want to do. 

```Python
dot = red_tuple
```

Now **dot** refers to **red_tuple**. The colour of **dot** can never change, because the colour in **red_tuple** cannot be changed.We can make immutable colour values to use in our programs:

```Python
RED = (255,0,0)
```

I can make things **RED** and be sure that they will always be **RED**. I don't have to worry whether or not something has fiddled with the contents of RED because they can't. It's a tuple. The only thing I have to worry about is if I assign RED to a list (perhaps the thing )

[home](/README.md)