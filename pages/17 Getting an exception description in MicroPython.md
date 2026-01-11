# Getting an exception description in MicroPython

This is useful if you want to find out how your otherwise perfect code has just fallen to pieces. One of the nice things about Python is that when a program fails you get a description of what happened and where:

```python
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "main.py", line 21, in <module>
NameError: name 'zanzibar' isn't defined
```
However, if you catch the exception you need a way of displaying this useful information in the handler. This is how you do it:

```python
try:
    mgr.setup(mgr.settings)
except Exception as e:
    print(f"[CLB] Manager {name} crashed during setup:")
    sys.print_exception(e)
```

The call of **sys.print_exception** takes in the exception object that was thrown and prints the terribly useful message. If you want to put the message into a string (perhaps so you can log it or send it somewhere) you can do this:

```python
import io
import sys
try:
    x=zanzibar
except Exception as e:
    buf = io.StringIO()
    sys.print_exception(e, buf)
    trace = buf.getvalue()
    print("bang")
    print(trace)
```
The code above will throw an exception (unless your program contains a variable called zanzibar). The exception is copied into the variable called **trace** which you can then do what you like with.


[home](/README.md)