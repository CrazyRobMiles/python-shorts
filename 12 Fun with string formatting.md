# 12 Fun with string formatting

We can use Python formatted string literals to easily drop values into strings of text. But we can also have even more fun with them when we add extra information to control the formatting process. This is particularly useful when we are creating messages to be displayed on devices with particular dimensions.  

For example. perhaps I want to display the time on an LCD panel. I want the hour and the minute to have leading zeroes (so that they look like a digital clock). I could write some cunning code to add the zeroes if the values are less than 10, or I could use a formatted string:
```
hour=5
minute=6
```
These are our time values. If we want to make a digital clock out of them we just need to do this:
```
time = f"{hour:02}:{minute:02}"
```
Note that each expression to be output is now followed by a colon and a couple of digits. The first digit means "Pad the number with zeroes". The second digit means "display the value in two spaces". So the time string is set to:
```
05:06
```
If we don't want to pad the number with zeros, but use spaces instead, we just omit the leading zero.
```
f"{0:10}"
```
This string literal ends up being 9 spaces followed by a single zero.

We can add a decimal point to our formatting values to control the number of decimal places displayed when using floating point values:
```
x=f"{3.141592653:10.3f}"
```
This would create a 10 character long string with a three decimal place value of the high-precision value of Pi:
```
'     3.142'
```
Note that the f after the 3 in the fornmat (the number of decimal places) tells Python that you are outputting a floating point number and it must have three decimal places. If you leave out the f Python assumes you are outputting a general value and will just display three digits (3.14).

Things get even better when we start using control characters to select the text alignment:
```
f"{'Menu':^10}"
```
This would centre the word Menu in a 10 character string. Jolly useful if you want to line things up for a particular sized LCD panel. You can use < and > to left or right justify the string inside the field. And it gets even funner (if that is a word). You can even use variables to control this formatting behaviour:
```
display_width=16
banner=f"{'Menu':^{display_width}}"
```
The above statements make a banner which is 16 characters long and contains the word Menu centred in it. If you want to change the size of the display you are using, just modify display_width

It is worth getting good with format strings, they can save an awful lot of work.

[back](/README.md)