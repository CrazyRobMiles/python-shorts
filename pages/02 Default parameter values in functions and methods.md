# Default parameter values in functions and methods

We’ve seen how to make parameters clearer in calls, now let’s add some magic to the function itself. Sometimes we might only have the name of the person, can we make an add_person which will handle only one input? Yes, we can.
```
def add_person(name, age=3):
    print("Adding a person")
```
The code above creates an add_person function which has name and age parameters. The age parameter is set to 3 if it is missed out. Programmers call the value 3 the “default” value.
```
add_person(name="Simon")
```
This would add a person with the name Simon with age 3. You may be wondering why I picked 3 as the default. If we were writing a system to control access to fairground rides, we want to make it as safe as possible. Simon would only be able to go on rides which are suitable for 3-year-olds. If they want to go on the bigger rides, they must give their age. 
```
add_person(name="Rob")
```
Note that if you want to use default values like these you must put the parameters with the default values at the end of the parameter list when the function is defined.

[home](/README.md)