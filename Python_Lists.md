# Python Lists

Lists are used to store multiple items in a single variable.

Lists are one of 4 built-in data types in Python used to store collections of data, the other 3 are `Tuple`, `Set`, and `Dictionary`, all with different qualities and usage.

Lists are created using square brackets:  
Example:  
```python
thislist = ["apple", "banana", "cherry"]
print(thislist)
```

### List Items
List items are ordered, changeable, and allow duplicate values.

List items are indexed, the first item has index `[0]`, the second item has index `[1]` etc.  

```python
thislist = ["apple", "banana", "cherry", "apple", "cherry"]
print(thislist)
```

### List Length
To determine how many items a list has, use the len() function:

Example:  
```python
thislist = ["apple", "banana", "cherry"]
print(len(thislist))
```

A list can contain different data types:

Example:
A list with strings, integers and boolean values:  
```python
list1 = ["abc", 34, True, 40, "male"]
```


### type()
From Python's perspective, lists are defined as objects with the data type 'list':

`<class 'list'>`  
Example:  
```python
mylist = ["apple", "banana", "cherry"]
print(type(mylist))     #Output: <class 'list'>
```


### The `list()` Constructor
It is also possible to use the `list()` constructor when creating a new list.

Example: 

```python
thislist = list(("apple", "banana", "cherry")) # note the double round-brackets
print(thislist)   #Output: ['apple', 'banana', 'cherry']
```



### Access List Items  
Negative Indexing  
Negative indexing means start from the end

`-1` refers to the `last` item, `-2` refers to the `second last` item etc.

Example:  

```python
thislist = ["apple", "banana", "cherry"]
print(thislist[-1])    #Output: cherry
```


### Range of Indexes  

You can specify a range of indexes by specifying where to start and where to end the range.

When specifying a range, the return value will be a new list with the specified items.

Example:    
```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:5])      #Output: ['cherry', 'orange', 'kiwi']
```
N.B: start at index 2 (included) and end at index 5 (not included).  


Example:
This example returns the items from the beginning to, but NOT including, "kiwi":
```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[:4])    #Output: ['apple', 'banana', 'cherry', 'orange']
```


By leaving out the end value, the range will go on to the end of the list:

Example:
This example returns the items from "cherry" to the end:
```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:])    #Output: ['cherry', 'orange', 'kiwi', 'melon', 'mango']
```


### Range of Negative Indexes

Example:  
This example returns the items from "orange" (-4) to, but NOT including "mango" (-1):
```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[-4:-1])     #Output: ['orange', 'kiwi', 'melon']
```


### Check if Item Exists
To determine if a specified item is present in a list use the `in` keyword:

Example:  
Check if "apple" is present in the list:
```python
thislist = ["apple", "banana", "cherry"]
if "apple" in thislist:
  print("Yes, 'apple' is in the fruits list")
```



### Change Item Value
To change the value of a specific item, refer to the index number:

Example:  
Change the second item:
```python
thislist = ["apple", "banana", "cherry"]
thislist[1] = "blackcurrant"
print(thislist)     #Output: ['apple', 'blackcurrant', 'cherry']
```


### Change a Range of Item Values
To change the value of items within a specific range, define a list with the new values, and refer to the range of index numbers where you want to insert the new values:

Example:  
Change the values "banana" and "cherry" with the values "blackcurrant" and "watermelon":
```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
thislist[1:3] = ["blackcurrant", "watermelon"]
print(thislist)     #Output: ['apple', 'blackcurrant', 'watermelon', 'orange', 'kiwi', 'mango']
```


If you insert more items than you replace, the new items will be inserted where you specified, and the remaining items will move accordingly:

Example:  
Change the second value by replacing it with two new values:
```python
thislist = ["apple", "banana", "cherry"]
thislist[1:2] = ["blackcurrant", "watermelon"]
print(thislist)       #Output: ['apple', 'blackcurrant', 'watermelon', 'cherry']
```



If you insert less items than you replace, the new items will be inserted where you specified, and the remaining items will move accordingly:

Example:  
Change the second and third value by replacing it with one value:
```python
thislist = ["apple", "banana", "cherry"]
thislist[1:3] = ["watermelon"]
print(thislist)   #Output: ['apple', 'watermelon']
```

-------------

## Insert Items
To insert a new list item, without replacing any of the existing values, we can use the `insert()` method.

The `insert()` method inserts an item at the specified index:

Example:   
Insert "watermelon" as the third item:
```python
thislist = ["apple", "banana", "cherry"]
thislist.insert(2, "watermelon")
print(thislist)     #Output: ['apple', 'banana', 'watermelon', 'cherry']
```
---------------
## Append Items
To add an item to the end of the list, use the `append()` method:

Example:    
Using the append() method to append an item:
```python
thislist = ["apple", "banana", "cherry"]
thislist.append("orange")
print(thislist)      #Output: ['apple', 'banana', 'cherry', 'orange']
```

------------------



## Extend List
To append elements from another list to the current list, use the extend() method.

Example:  
Add the elements of tropical to thislist:
```python
thislist = ["apple", "banana", "cherry"]
tropical = ["mango", "pineapple", "papaya"]
thislist.extend(tropical)
print(thislist)         #Output: ['apple', 'banana', 'cherry', 'mango', 'pineapple', 'papaya']
```


## Remove List Items

The `remove()` method removes the specified item.

Example:  
Remove "banana":
```python
thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)     #OUTPUT: ['apple', 'cherry']
```


If there are more than one item with the specified value, the remove() method removes the first occurrence:

Example:  
Remove the first occurrence of "banana":
```python
thislist = ["apple", "banana", "cherry", "banana", "kiwi"]
thislist.remove("banana")
print(thislist)     #Output: ['apple', 'cherry', 'banana', 'kiwi']
```



## Remove Specified Index  
The `pop()` method removes the specified index.

Example:   
```python
thislist = ["apple", "banana", "cherry"]
thislist.pop(1)
print(thislist)    #Output: ['apple', 'cherry']
```
But,  
If you do not specify the index, the `pop()` method removes the last item.

Example:  
```python
thislist = ["apple", "banana", "cherry"]
thislist.pop()
print(thislist)   #Output: ['apple', 'banana']
```


The `del` keyword also removes the specified index:

Example:  
```python
thislist = ["apple", "banana", "cherry"]
del thislist[0]
print(thislist)  #Output: ['banana', 'cherry']
```

The `del` keyword can also delete the list completely.

Example:  
```python
thislist = ["apple", "banana", "cherry"]
del thislist
```


### Clear the List
The `clear()` method empties the list.

The list still remains, but it has no content.

Example:  
```python
thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)   #Output: []
```


## Loop Through a List  
You can loop through the list items by using a for loop:

Example:  
```python
thislist = ["apple", "banana", "cherry"]
for x in thislist:
  print(x)
```


### Loop Through the Index Numbers
You can also loop through the list items by referring to their index number.

Use the range() and len() functions to create a suitable iterable.

Example:  
```python
thislist = ["apple", "banana", "cherry"]
for i in range(len(thislist)):
  print(thislist[i])
```


### Using a While Loop
You can loop through the list items by using a while loop.

Example:  
```python
thislist = ["apple", "banana", "cherry"]
i = 0
while i < len(thislist):
  print(thislist[i])
  i = i + 1
```

### Looping Using List Comprehension

Example:  
```python
thislist = ["apple", "banana", "cherry"]
[print(x) for x in thislist]
```


## List Comprehension
List comprehension offers a shorter syntax when you want to create a new list based on the values of an existing list.

Example:

Based on a list of fruits, you want a new list, containing only the fruits with the letter "a" in the name.

Example:  
```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
  if "a" in x:
    newlist.append(x)
print(newlist)     #Output: ['apple', 'banana', 'mango']
```


With list comprehension you can do all that with only one line of code:

Example:  
```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x for x in fruits if "a" in x]

print(newlist)
```


