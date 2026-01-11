# Formatted string literals

Formatted string literals are amazingly useful. You can make your Python output look really good, whether you are printing on the terminal or assembling a message to be displayed on an embedded display. 

There are several ways to create formatted literals. I like the “f-string” approach which works in later versions of the language, including MicroPython and CircuitPython. 

Let’s start with some values we might want to output:
```
name="Rob"
age=21
```
We can create a formatted string to display this values as follows:
```
message = f"Name:{name} Age:{age}"
```
The f in front of the string tells Python to scan the string and look for braces (curly brackets) that identify expression values to be included in the string. The values of name and age are inserted into the string in the specified positions. If you actually want to put braces into your text you have to enter two of them:
```
age_braces = f"{{{age}}}"
```
This would create a string containing the value of age enclosed in braces.

[Fun with string formatting](/pages/12%20Fun%20with%20string%20formatting.md)

[home](/README.md)