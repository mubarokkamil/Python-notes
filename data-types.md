# Built-in Data Types:
In programming, **data type** is an important concept.  
Variables can store data of different types, and different types can do different things.

Python has the following **built-in data types** by default, in these categories:

- **Text Type:** `str`  
- **Numeric Types:** `int`, `float`, `complex`  
- **Sequence Types:** `list`, `tuple`, `range`  
- **Mapping Type:** `dict`  
- **Set Types:** `set`, `frozenset`  
- **Boolean Type:** `bool`  
- **Binary Types:** `bytes`, `bytearray`, `memoryview`  
- **None Type:** `NoneType`


# Getting the Data Type:
You can get the **data type** of any object by using the `type()` function  
Ex:  
```python
x = 5
print(type(x))
```
**Output:**
```
<class 'int'>
```


# Random Number

Python does not have a built-in `random()` function, but it has a **`random` module** that can be used to generate random numbers.
## 1️⃣ random.randrange()

```python
import random

print(random.randrange(1, 10))  #Output: 7
```
#### ✅ Explanation:
- `random.randrange(1, 10)` returns a random integer from `1 to 9 (10 is excluded)`.
- Each time you run the code, you may get a different number.

## 2️⃣ random.randint()

Returns a random integer between two values (both included).  
```python
import random
print(random.randint(1, 10))
```

## 3️⃣random.choice()

Returns a random item from a sequence (list, tuple, or string).  
```python
import random
fruits = ["apple", "banana", "cherry"]
print(random.choice(fruits))  #Output: banana
```

## 4️⃣random.uniform()
Returns a random floating-point number between two numbers.  
```python
import random
print(random.uniform(1, 10)) #Output: 6.3452
```

