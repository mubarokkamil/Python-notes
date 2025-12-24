# Python Operators

## Arithmetic Operators

Arithmetic operators are used with numeric values to perform common mathematical operations.
| Operator | Name           | Example |
|----------|----------------|---------|
| +        | Addition       | x + y   |
| -        | Subtraction    | x - y   |
| *        | Multiplication | x * y   |
| /        | Division       | x / y   |
| %        | Modulus        | x % y   |
| **       | Exponentiation | x ** y  |
| //       | Floor Division | x // y  |

Example:  
```python
x = 15
y = 4

print(x + y)   # 19
print(x - y)   # 11
print(x * y)   # 60
print(x % y)   # 3
print(x ** y)  # 15⁴ = 50625
```


Python has two division operators, each behaving differently:

1. `/` – Division (Returns a Float)

     - Always returns a floating-point number, even if the result is a whole number.
  
2. `//` – Floor Division (Returns an Integer)

Example:  
```python
a = 7
b = 2

print(a / b)      #Output: 3.5
print(a // b)     #Output: 3
```


## Assignment Operators

Assignment operators are used to assign values to variables.

| Operator | Example   | Same As      |
| -------- | --------- | ------------ |
| =        | x = 5     | x = 5        |
| +=       | x += 3    | x = x + 3    |
| -=       | x -= 3    | x = x - 3    |
| *=       | x *= 3    | x = x * 3    |
| /=       | x /= 3    | x = x / 3    |
| %=       | x %= 3    | x = x % 3    |
| //=      | x //= 3   | x = x // 3   |
| **=      | x **= 3   | x = x ** 3   |
| &=       | x &= 3    | x = x & 3    |
| ^=       | x ^= 3    | x = x ^ 3    |
| >>=      | x >>= 3   | x = x >> 3   |
| <<=      | x <<= 3   | x = x << 3   |



### The Walrus Operator `(:=)`

Python 3.8 introduced a new operator called the walrus operator `:=`.

The walrus operator allows you to assign a value to a variable and use it at the same time inside an expression.

Example:  
Normal Assignment:  
```python
x = 5
print(x)
```
Using Walrus Operator:  
```python
print(x := 5)
```

Example:  
```python
text = "Hello, Python!"
if (n := len(text)) > 10:
    print(f"Length is {n}, which is more than 10")
```

✅ Step by step explanation:

- `len(text)` calculates the length → 14

- `(n := len(text))` assigns 14 to n and evaluates it for the if condition

- `> 10` checks if 14 > 10 → True

- Prints


## Python Comparison Operators

Comparison operators are used to compare two values. They return **True** or **False** depending on the comparison.

| Operator | Name                      | Example  | Explanation                  |
|----------|---------------------------|----------|-----------------------------|
| ==       | Equal                     | x == y   | True if x is equal to y     |
| !=       | Not equal                 | x != y   | True if x is not equal to y |
| >        | Greater than              | x > y    | True if x is greater than y |
| <        | Less than                 | x < y    | True if x is less than y    |
| >=       | Greater than or equal to  | x >= y   | True if x is greater or equal to y |
| <=       | Less than or equal to     | x <= y   | True if x is less or equal to y |

---

Examples:

```python
x = 10
y = 5

print(x == y)   # False
print(x != y)   # True
print(x > y)    # True
print(x < y)    # False
print(x >= y)   # True
print(x <= y)   # False
```


## Python Logical Operators

Logical operators are used to combine conditional statements. They return **True** or **False** depending on the conditions.

| Operator | Description                                    | Example                   |
|----------|-----------------------------------------------|---------------------------|
| and      | Returns True if **both** statements are true | x < 5 and x < 10          |
| or       | Returns True if **one** of the statements is true | x < 5 or x < 4        |
| not      | Reverses the result; returns False if the result is true | not(x < 5 and x < 10) |

---

Examples:

```python
x = 4
y = 10

print(x < 5 and y < 15)   # True, both conditions are True
print(x < 5 or y < 5)     # True, one condition is True
print(not(x < 5))         # False, not reverses the True result
```



## Python Identity Operators

Identity operators are used to compare **objects**, not just values.  
They check whether two variables point to the **same object in memory**.

| Operator | Description                                       | Example   |
|----------|--------------------------------------------------|-----------|
| is       | Returns True if both variables are the same object | x is y    |
| is not   | Returns True if both variables are not the same object | x is not y |

---

Examples:

```python
x = ["apple", "banana"]
y = ["apple", "banana"]
z = x

print(x is z)      # True, z references the same object as x
print(x is y)      # False, x and y have the same content but are different objects
print(x is not y)  # True, x and y are not the same object
```



### Difference Between `is` and `==`

In Python, `is` and `==` are often confused but they are different:

- `is` → Checks if both variables **point to the same object in memory**  
- `==` → Checks if the **values of both variables are equal**

---

## Example

```python
x = [1, 2, 3]
y = [1, 2, 3]

print(x == y)   # True, because the values are the same
print(x is y)   # False, because x and y are different objects in memory
```


# Membership Operators

Membership operators are used to test whether a value or sequence exists inside another object (such as a string, list, tuple, or set).



| Operator | Description                                                                 | Example        |
|---------|-----------------------------------------------------------------------------|----------------|
| `in`    | Returns `True` if the specified value is present in the object               | `x in y`       |
| `not in`| Returns `True` if the specified value is NOT present in the object           | `x not in y`   |



### Example 1: Using `in`
```python
fruits = ["apple", "banana", "cherry"]

print("banana" in fruits)   # True
print("mango" in fruits)    # False
```

### Example 2: Using `not in`
```python
text = "Hello, World!"

print("Python" not in text)   # True
print("Hello" not in text)    # False
print("H" in text)        # True
print("hello" in text)    # False (case-sensitive)
print("z" not in text)    # True
```


## Bitwise Operators

Bitwise operators are used to perform operations on numbers at the **binary (bit) level**.

---

### List of Bitwise Operators

| Operator | Name | Description | Example |
|--------|------|------------|--------|
| `&` | AND | Sets each bit to `1` if **both** bits are `1` | `x & y` |
| `|` | OR | Sets each bit to `1` if **one** of the bits is `1` | `x | y` |
| `^` | XOR | Sets each bit to `1` if **only one** bit is `1` | `x ^ y` |
| `~` | NOT | Inverts all the bits | `~x` |
| `<<` | Left Shift | Shifts bits left, filling with zeros on the right | `x << 2` |
| `>>` | Right Shift | Shifts bits right, preserving the sign bit | `x >> 2` |

---

### 1️⃣ Bitwise AND `(&)`  

```
5 & 3:

  0101   (5)
& 0011   (3)
------
  0001
```
Rule:  
- `AND` returns 1 only if both bits are 1.

### 2️⃣ Bitwise OR (`|`)
```
5 | 3

  0101
| 0011
------
  0111
```

Rule:  
- `OR` returns 1 if any one bit is 1.

### 3️⃣ Bitwise XOR (`^`)
```
5 ^ 3

  0101
^ 0011
------
  0110
```

Rule:  
- `XOR` returns `1` only if bits are different.
- `XOR` returns `0` only if bits are same. 
    - 1 ^ 1 = 0
    - 1 ^ 0 = 1


### 4️⃣ Bitwise NOT (~)
```
~5 = 00000101
```
```
After NOT (flip every bit):
11111010
```
#### ✅Explanation:
Python represents negative numbers using 2’s complement.  
Because of this rule, the bitwise NOT (~) operator follows a simple formula:

`~x = -(x + 1)`

Step 1:   

The `~` operator flips every bit:

1 → 0

0 → 1

Step 2:   
Look at the number 5 in binary
5 = 00000101

Step 3:   
Apply bitwise NOT (~)

Flip every bit:  
```
  00000101   (5)
~ --------
  11111010
```

This binary number starts with 1,
so Python treats it as a negative number.

Step 4:   
How Python interprets this negative number

Python uses 2’s complement to convert this binary back to decimal.

Instead of doing all binary math, Python follows this shortcut rule:

`~x = -(x + 1)`

So for x = 5:

~5 = -(5 + 1)
~5 = -6
------- 

### 5️⃣ Left Shift (`<<`)
```
5 << 1 means,
Shift bits left by 1 position:

0101  →  1010
```
Shifting left by 1 means:

5 × 2 = 10  
✅ Result: 10


### 6️⃣ Right Shift (`>>`)
```
5 >> 1 means,
Shift bits right by 1 position:

0101  →  0010
```
Shifting right by 1 means:

5 ÷ 2 = 2


### Example

```python
x = 5   # Binary: 0101
y = 3   # Binary: 0011

print(x & y)   # 1
print(x | y)   # 7
print(x ^ y)   # 6
print(~x)      # -6
print(x << 1)  # 10
print(x >> 1)  # 2
```


## Operator Precedence in Python

Operator precedence determines the order in which operations are evaluated in an expression.
Operators with higher precedence are evaluated before operators with lower precedence.

Precedence Order (Highest → Lowest):  
| Operator                                      | Description                                       |            
| -------------------------------------------- | ------------------------------------------------- |            
| ()                                           | Parentheses                                       |            
| **                                           | Exponentiation                                    |            
| +x  -x  ~x                                   | Unary plus, unary minus, bitwise NOT              |            
| *  /  //  %                                  | Multiplication, division, floor division, modulus |            
| +  -                                         | Addition and subtraction                          |            
| <<  >>                                       | Bitwise left and right shifts                     |            
| &                                            | Bitwise AND                                       |            
| ^                                            | Bitwise XOR                                       |            
| ==  !=  >  >=  <  <=  is  is not  in  not in | Comparison, identity, membership                  |            
| not                                          | Logical NOT                                       |            
| and                                          | Logical AND                                       |            
| or                                           | Logical OR                                        |            


### Left-to-Right Evaluation Rule

If two operators have the same precedence, Python evaluates them from left to right.

Example: Same Precedence Operators

Addition (+) and subtraction (-) have the same precedence,
so Python evaluates the expression from left to right.

Example:  
print(5 + 4 - 7 + 3)

Step-by-Step Evaluation
- 5 + 4 = 9
- 9 - 7 = 2
- 2 + 3 = 5


