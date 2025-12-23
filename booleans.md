# Python Booleans
Booleans represent one of two values: True or False.

```python
print(10 > 9)
print(10 == 9)
print(10 < 9)
```

## Evaluate Values and Variables
The `bool()` function allows you to evaluate any value, and give you True or False in return  

### Most Values are True

Almost any value is evaluated to True if it has some sort of content.

Any string is True, except empty strings.

Any number is True, except 0.

Any list, tuple, set, and dictionary are True, except empty ones.

```python
print(bool("Hello")) #Output: True
print(bool(15))    #Output: True
```

### Some Values are False
In fact, there are not many values that evaluate to False, except empty values, such as `(), [], {}, ""`, the number `0`, and the value `None`. And of course the value `False` evaluates to False.

