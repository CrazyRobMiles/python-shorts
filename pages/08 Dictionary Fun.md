# 08 Dictionary Fun

Dictionaries are fun. As we saw last time we can use them to create lumps of data with named contents:
```
z={"name":"Anne","age":21}
```
This makes a dictionary called z with two things inside it, name and age. We can get these out by name (as it were):
```
n = z["name"]
```
One thing to watch out for is that you need to get the search item (or key as it is called) exactly right:
```
n = z["Name"]
```
This would end badly, with an exception which will stop your program:
```
KeyError: name
```
If you are worried about your program crashing when you try to get something out of a dictionary, you can use the in operator to check:
```
if "name" in z:
  print("we have a name")
```
As a side note, I’m using square brackets to enclose the key we want to find. You can use the get function instead:
```
n = z.get("name")
```
This would set n to the name in z.

[Dictionary Madness](/pages/09%20Dictionary%20Madness.md)

[home](/README.md)