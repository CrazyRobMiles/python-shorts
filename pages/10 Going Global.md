# 10 Going Global

A variable is a box you can name to put something in. In Python you can just make one:
```
 age=21
```
Python decides it needs to make a variable (age is not a word Python knows), looks at 21, decides that it needs an integer shaped box, makes one,  puts 21 in it and then paints the word age on the box so it can find age later. So far, so normal. Let’s make a function:
```
 def brokenFunc():
    print(age)
```
There’s a clue here that bad things are about to happen. If you run this you get: 

UnboundLocalError: cannot access local variable 'age' where it is not associated with a value

This is because the body of a function (the indented bit after def) is a separate variable scope. The scope of a variable is those areas of your code where statements can work with it.  Any variables created in a function body are local to the function and disappear when the function completes. Variables are either global (declared outside all functions) or local (declared inside the body of a function). If you want to be able to access global variables inside a function body you need to tell Python
```
 def mendedFunc():
    global age
    print(age)
```
Code in the body of mendedFunc function can now access age (and also change it). Forcing programmers to explicitly state when they are using global resources in their code helps prevent errors which would be caused if the same variable name is used in more then one context. If one part of the program is manipulating the age of a person, and another part of the program is manipulating the age of the house they want to buy, we don’t want these getting mixed up when the program runs. 

[home](/README.md)