# Rules for Python variables:

1. A variable name must start with a letter or the underscore character
2. A variable name cannot start with a number
3. A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
4. Variable names are case-sensitive (age, Age and AGE are three different variables)
5. A variable name cannot be any of the Python keywords.

## Python Variable Naming Conventions

#### Camel Case:
Each word, except the first, starts with a capital letter:  
```python
myVariableName = "John"
```

#### Pascal Case:
Each word starts with a capital letter:
```python
MyVariableName = "John"
```

#### Snake Case:
Each word is separated by an underscore character:
```python
my_variable_name = "John"
```

#### Python allows you to assign values to multiple variables in one line:
Ex:
```python
x, y, z = "Orange", "Banana", "Cherry"
```

#### And you can assign the same value to multiple variables in one line:
Ex:
```python
x = y = z = "Orange"
```

## Unpack a Collection:
If you have a collection of values in a list, tuple etc. Python allows you to extract the values into variables. This is called unpacking.

Ex:
```python
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(x)
print(y)
print(z)
```
**Output:**

```
apple
banana
cherry
```

## Printing Multiple Variables
In the `print()` function, you output multiple variables, separated by a **comma**:

Example:
```python
x = "Python"
y = "is"
z = "awesome"
print(x, y, z)  #Output: Python is awesome
```

You can also use the `+` operator to output multiple variables:

Example:
```python
x = "Python "
y = "is "
z = "awesome"
print(x + y + z)  #Output: Python is awesome
```

#### Note:

✅ Use **comma in `print()`** to automatically add spaces between variables.  


# Global Variables:

Variables that are created outside of a function (as in all of the examples in the previous) are known as **global variables**.  
Global variables can be used by everyone, both inside of functions and outside.

If you create a variable with the same name inside a function, this variable will be **local**, and can only be used inside the function. The global variable with the same name will remain as it was, global and with the original value.
Ex:
```python
x = "awesome"

def myfunc():
  x = "fantastic"
  print("Python is " + x)

myfunc()

print("Python is " + x)
```

**Output:**
```
Python is fantastic
Python is awesome
```
#### ✅ Explanation:

- The first `x` inside `myfunc()` is local, so it does not change the global `x`.
- The global `x` remains `"awesome"` outside the function.

## use the `global` keyword if you want to change a global variable inside a function:
Ex:
```python
x = "awesome"

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```

**Output:**
```
Python is fantastic
```
#### ✅ Explanation:
- The global keyword tells Python that x inside the function refers to the global variable.
- Therefore, modifying x inside myfunc() changes the global variable.
- After the function runs, x is "fantastic" globally.


