# Dictionaries

You may have spotted a problem with lists and tuples. When we talked about functions we worried about the situation where we use the wrong order of parameters to a call. We can get the same problem with lists and tuples:

The statement above would set the age of person y to “James”, which would not be a good thing if the age value was stored in location 1. It would be lovely if we had a data structure that let us explicitly name the data elements in it. It turns out that we do, and it is called a dictionary:
```
z={"name":"Anne","age":21}
```
When you make a dictionary you give it a set of key – value pairs. This means that everything that is stored has a name – the key which is used to access it. The dictionary referred to by z has two keys, name and age. You can use these to get hold of the values:
```
n = z["name"]
```
The above statement gets the value of the name item in z. In this case the value of n would be “Anne”. 

[Dictionary Fun](/pages/08%20Dictionary%20Fun.md)

[home](/README.md)