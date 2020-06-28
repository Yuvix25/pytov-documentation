# Pytov functions

## Switch

Instead of using tons of if elses, in pytov you can use the switch statement.  
The switch statement in pytov is function, which you call with 2 - 3 arguments, value to switch on, cases, and optionally default case (by order).  

* value - anything
* cases - a dictionery of values and callbacks
* default case - a callback

The switch will find the case key that matches the given value, and execute its callback, if no key matches the value and default case exists, it will call the default case.  
### Example 1 (default case not called):

```python
switch("sample", {
    "example": lambda { print("not this one...") },
    "banana": lambda { print("thats not it") },
    "sample": lambda { print("found it!") },
},  
    lambda { print("the default case will not execute, beacuse the switch found 'sample' inside the cases") },
)
```
### Example 2 (default case called):

```python
switch("sample", {
    "example": lambda { print("not this one...") },
    "banana": lambda { print("thats not it") },
    "notsample": lambda { print("so close!") },
},
    lambda { print("i'm called because there was no match in the cases.") },
)
```
---
[Back to main page](index.md)