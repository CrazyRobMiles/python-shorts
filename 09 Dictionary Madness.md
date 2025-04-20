# 09 Dictionary Madness

You can have all kinds of fun with dictionaries. 

First off, you can add things to a dictionary any time you like:
```
z={"name":"Anne","age":21}
```
This makes a dictionary called z
```
z["address"]="18 Pussycat Mews"
```
This adds an address item to the dictionary. But for super fun you can use any kind of value as a key for an item:
```
z[1.5]="This is crazy"
```
This uses the value 1.5 as a key. What with computer floating point maths not being as accurate as you might like, using floating point values as keys to dictionary entries is not advisable, but using integers can be very sensible. And if you are doing things like counting the number of letters in text, or putting ranges of values into buckets you can use dictionaries to very good effect. 

[home](/README.md)