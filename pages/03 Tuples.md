# 03 Tuples

Tuples should be called “lumps”. You can squish things together to make a lump. Tuples let you squish data together.
```
x = ("Jim",25)
```
The statement above creates a tuple called x which contains name and age information. Tuples can contain lots of data. The best way to unpick them is to use a cunning assignment:
```
(name,age)=x
```
This creates variables called name and age which hold “Jim” and 25 respectively.  Another way to get values out of a tuple is to index it:
```
name=x[0]

age=x[1]
```
The item at the start of the tuple has index value 0. Tuples are read only:
```
x[0]="James"
```
The statement above tries to change the in the x tuple. This will not work. Tuples are great for passing lumps of data around a program but no good for things you might want to modify. If you want to be able to change things in a lump of data you need use a list. 

I find tuples very useful, but I do worry that the thing making the tuple and the thing using the tuple have to agree on the order of the elements. As we saw with name and age in function parameters this might lead to confusion. If you want both ends of a conversation to be absolutely clear about which data means what, you can use dictionaries to do that, but they are coming later. 

[Tuple of one](/pages/04%20Tuple%20of%20One.md)

[home](/README.md)