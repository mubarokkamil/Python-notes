# Looping Through a String

Since strings are arrays, we can loop through the characters in a string using a `for` loop.

#### Example

```python
for x in "banana":
    print(x)
```

**Output:**
```
b
a
n
a
n
a
```

# String Length:
To get the length of a string, use the  `len()` function.  
Ex:  
```python
a = "Hello, World!"
print(len(a))
```

# Check String

To check if a certain phrase or character is present in a string, we can use the `in` keyword.

#### Example

```python
txt = "The best things in life are free!"
print("free" in txt)  #Output: True
```

## using `if`  
```python
txt = "The best things in life are free!"
if "free" in txt:
    print("Yes, 'free' is present.")
```

#### ✅Explanation
- The `in` keyword checks whether a value exists inside a string.
- It returns `True` if the value is found, otherwise `False`.


## Check if NOT

To check if a certain phrase or character is **NOT** present in a string, we can use the `not in` keyword.

### Example

```python
txt = "The best things in life are free!"
if "expensive" not in txt:
    print("No, 'expensive' is NOT present.")
```

# Python – Slicing Strings

You can return a range of characters by using the **slice syntax**.  
Specify the **start index** and the **end index**, separated by a colon (`:`), to return part of a string.

### Example

```python
b = "Hello, World!"
print(b[2:5])  # llo
```

#### ✅Explanation
- Indexing in Python starts from 0.  
- `b[2:5]` means:

   - Start from index 2 (character l)

   - Stop at index 5 (character at index 5 is not included)


## Slice with Step

You can also specify the **step value** in slicing.  
The step determines how many characters to skip while slicing.

#### Syntax:

```python
string[start:end:step]
```

#### Example:

```python
b = "Hello, World!"
print(b[0:12:2])   #Output: Hlo ol
```

#### ✅Explanation
- start = 0 → slicing starts from the first character
- end = 12 → slicing stops before index 12
- step = 2 → every second character is selected
- This means Python picks characters at index 0, 2, 4, 6, 8, 10


## Slice From the Start

By leaving out the **start index**, slicing begins from the **first character** of the string.

#### Example:

```python
b = "Hello, World!"
print(b[:5])    #Output: Hello
```

#### ✅Explanation

- `:5` means start from index 0
- Characters are taken up to index 5 (not included)


## Slice To the End

By leaving out the end index, slicing continues until the end of the string.  
#### Example:

```python
b = "Hello, World!"
print(b[2:])     #Output: llo, World!
```

#### ✅Explanation

- `2:` means start from index 2
- All characters from index 2 to the end are included



## Negative Indexing

**Negative indexing** allows you to start slicing from the **end of the string**.

- `-1` → last character  
- `-2` → second last character  
- and so on…

---

#### Example:

```python
b = "Hello, World!"
print(b[-5:-2])      #Output: orl
```


#### 🧠 Explanation

- `-5` → character "o" in "World!"
  
- `-2` → character "d" in "World!"
- Negative indexes count from the end
- The ending index is excluded
- Very useful when the string length is unknown



# Python - Modify Strings

### Upper-Case
The `upper()` method returns the string in upper case.

```python
a = "Hello, World!"
print(a.upper())      #Output: HELLO, WORLD!
```


### Lower-Case

The `lower()` method returns the string in lower case.  
```python
a = "Hello, World!"
print(a.lower())     #Output: hello, world!
```


### Remove Whitespace

The `strip()` method removes any whitespace from the beginning or the end.

```python
a = " Hello, World! "
print(a.strip())    # Output: "Hello, World!"
```


### Replace String

The `replace()` method replaces a string with another string.

```python
a = "Hello, World!"
print(a.replace("H", "J"))  # 'J' will replace 'H'
#Output: Jello, World!
```


### Split String

Split String is used to break a single string into a list of smaller strings based on a specific pattern or character.

#### Example: (Splitting by Hyphen)

```python
text = "apple-banana-cherry"
fruits = text.split("-")
print(fruits)
```
Output: 
```
['apple', 'banana', 'cherry']
```

**Example: (Splitting by Comma)**

```python
text = "apple,banana,cherry"
fruits = text.split(",")
print(fruits)
```
Output:
```
['apple', 'banana', 'cherry']
```


# String Concatenation

In Python, string concatenation means joining two or more strings together to create a new string.  
There are several ways to do this, ranging from simple operators to modern formatting methods:

### 1. Using the `+` Operator
This is the most common and simplest way to join strings.

```python
a = "Hello"
b = "World"
c = a + b
print(c)  # Output: HelloWorld
```

### 2. Using the `join()` Method

This is the most efficient method when you have a list of many strings to join.
```python
words = ["Python", "is", "awesome"]
result = " ".join(words)  # The string before .join() is the separator
print(result)             # Output: Python is awesome

csv_style = ",".join(words)
print(csv_style)          # Output: Python,is,awesome
```

### 3. Using the Comma `,` in print()

When using the `print()` function, you can use commas. Python will automatically add a space between the items.

```python
print("Hello", "World")  # Output: Hello World
```


### 4. Using the `+=` Operator

This is used to append a string to the end of an existing string variable.

```python
msg = "Hello"
msg += " Python"
print(msg)  # Output: Hello Python
```



# Python - Format Strings

To specify a string as an f-string, simply put an `f` in front of the string literal, and add curly brackets `{}` as placeholders for variables and other operations.  
**Syntax:** `f"{var}"`

Example :
```python
age = 36
txt = f"My name is John, I am {age}"
print(txt)  # Output: My name is John, I am 36
```


A placeholder can include a modifier to format the value. A modifier is included by adding a colon : followed by a legal formatting type, like .2f which means fixed-point number with 2 decimals.

Example:  
```python
price = 59
txt = f"The price is {price:.2f} dollars"
print(txt)  # Output: The price is 59.00 dollars
```

# Common Escape Characters

| Escape Sequence | Meaning         |
| --------------- | --------------- |
| `\'`            | Single Quote    |
| `\"`            | Double Quote    |
| `\\`            | Backslash       |
| `\n`            | New Line        |
| `\r`            | Carriage Return |
| `\t`            | Horizontal Tab  |
| `\b`            | Backspace       |
| `\f`            | Form Feed       |
| `\ooo`          | Octal value     |
| `\xhh`          | Hex value       |

