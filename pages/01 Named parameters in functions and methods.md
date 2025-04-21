## 01 Named parameters in functions and methods
Python functions and methods can accept parameters that feed data into them. But once you have more than one parameter it can get tricky. For example, perhaps we have a function called add_person which adds a person to our system. The function accepts the name and the age of the person: 

```
add_person("Jim",12)
```

This would add Jim to the system. But what happens if I get the call wrong?

```
add_person(12,"Fred")
```

The code and the name have been entered in the wrong order.  We are making someone with the name “21” and the age “Fred”. This will end in tears. The good news is that Python lets you specify the parameter name in the call:

```
add_person(name="Jim",age=21)
```

Now the destinations are explicitly defined and there is no chance of error and the code is much clearer.

[Default Parameter Values](/pages/02%20Default%20parameter%20values%20in%20functions%20and%20methods.md)

[home](/README.md)