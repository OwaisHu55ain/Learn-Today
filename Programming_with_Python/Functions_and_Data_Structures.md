# Functions and Data Structures

Functions in Python encapsulate reusable blocks of code for specific tasks, enhancing code modularity and readability. Data structures, such as lists and dictionaries, enable organized storage and manipulation of data, facilitating efficient information management in Python programs.


## Functions

A block of code that performs a specific task or set of tasks.


```
# define function for calculating the tax
def calculate_tax(bill_amount, tax_rate):
    total_tax = (bill_amount*tax_rate)/100
    print(f'Total Tax = {total_tax}')

calculate_tax(100.00, 20.00)
```

## Variable Scope
A variable scope refers to the region or part of program where variable can be accessed and used. There are four types of Scopes:


## 1. Local Scope (L): 
A local scope refers to the region of a program where a variable is defined and can be accessed. Variables created within a function or a block of code have local scope, meaning they are only visible and usable within that specific function or block. Outside of that scope, the variable is not accessible. This concept helps prevent unintended variable conflicts and allows for more modular and maintainable code.

```
def get_total(a, b):
    #local variable declared inside a function
    total = a + b;
    return total

print(get_total(5, 2))
7

 # Accessing variable outside of the function:

print(total)
NameError: name 'total' is not defined
```


## 2. Enclosing Scope (E): 
The enclosing scope in Python refers to the scope that surrounds a nested function. If a function is defined within another function, the outer function's scope is considered the enclosing scope for the inner function. This allows the inner function to access variables from the outer function, but those variables are not directly accessible outside the outer function. Enclosing scope helps maintain the separation of concerns and supports the concept of closures in Python.

```
def get_total(a, b):
    #enclosed variable declared inside a function
    total = a + b

    def double_it():
        #local variable
        double = total * 2
        print(double)

    double_it()
    #double variable will not be accessible
    print(double)

    return total
```


## 3. Global Scope (G): 
The global scope refers to the outermost level of a program, where variables are defined outside of any function or block. Variables in the global scope are accessible from any part of the code, including functions. However, if a variable is modified within a function without using the global keyword, a new local variable with the same name is created inside that function, and it does not affect the global variable with the same name. The global scope is the broadest level of visibility in a Python program.

```

special = 5

def get_total(a, b):
    #enclosed scope variable declared inside a function
    total = a + b
    print(special)

    def double_it():
        #local variable
        double = total * 2
        print(special)

    double_it()

    return total
```

## 4: Built-in Scope (B): 
The built-in scope in Python refers to the namespace that contains the names of built-in functions, exceptions, and other entities that are part of the Python language itself. These names are always available without the need to import any module.


## Data Structure
A data structure allows you to organize and arrange your data to perform operation on them. Types of Data Structure are as following:

1. Mutable Data: Refers to the data inside the data structure can be modified.
2. Immutable Data: An immutable data structure will not allow modification once the data has been set.


## List
List data types represents an ordered collection of items. List element can contain different data types and are mutable.


Here are some common list functions and operations:
1. **len() **
Returns the numbers elements in a list.
```
inventory = ['Books', 'Pencil', 'Eraser', 'Scale']

print(len(inventory))
```


2. **append()**
Add an element at the end of the list.
```
inventory = ['Books', 'Pencil', 'Eraser', 'Scale']
inventory.append('Sharpners')
print(inventory) #output: ['Books', 'Pencil', 'Eraser', 'Scale', 'Sharpners']
```


3. **insert()**
Insert an element at a specific index.
```
inventory = ['Books', 'Pencil', 'Eraser', 'Scale']
inventory.insert(1,'Sharpner')
print(inventory) #output: ['Books', 'Sharpner', 'Pencil', 'Eraser', 'Scale']
```


4. **remove()**
Remove the first occurrence of a specified element from the list.
```
inventory = ['Books', 'Pencil', 'Eraser', 'Scale', 'Pencil']
inventory.remove('Pencil')
print(inventory) #output: ['Books', 'Eraser', 'Scale', 'Pencil']
```


5. **pop()**
Remove and return the element at a specific index (by default, the last element).
```
inventory = ['Books', 'Pencil', 'Eraser', 'Scale']
inventory.pop(1)
print(inventory) #output: ['Books', 'Eraser', 'Scale']
```


6. **index()**
Returns the index of the first occurrence of specified element.
```
inventory = ['Books', 'Pencil', 'Eraser', 'Scale']
print(inventory.index('Pencil')) #output: 1
```


7. **count()**
Returns the number of occurrences of specified element in the list.
```
names = ['John', 'Cena', 'John', 'John', 'Owais', 'Kamil']
print(names.count('John')) # Output: 3
```


8. **sort()**
Sort the list in ascending order (or based on custom sorting function).
```
 # Example 1
inventory = ['Books', 'Pencil', 'Eraser', 'Scale']
inventory.sort()
print(inventory) #output: ['Books', 'Eraser', 'Pencil', 'Scale']

 # Example 2
numbers = [4,3,2,1]
numbers.sort()
print(numbers) #output: [1,2,3,4]
numbers.sort(reverse=True)
print(numbers) #output: [4,3,2,1]
```



9. **reverse()**
Reverse the order of element in the list.
```
names = ['John', 'Cena', 'John', 'John', 'Owais', 'Kamil']
names.sort()
print(names) # Output: ['Cena', 'John', 'John', 'John', 'Kamil', 'Owais']
names.reverse()
print(names) #  Output: ['Owais', 'Kamil', 'John', 'John', 'John', 'Cena']
```


10. **copy()**
Create a shallow copy of a list.

```
names = ['John', 'Cena', 'John', 'John', 'Owais', 'Kamil']
print(*names) # output: John Cena John John Owais Kamil
my_names = names.copy()
print(*my_names) # output: John Cena John John Owais Kamil
```


## Tuple
A tuple is an ordered, immutable, and heterogeneous collection of elements. Tuples are defined using parenthesis. 

```
my_tuple = (1, 'Owais', 2.2, True)

print(my_tuple) #output: (1, 'Owais', 2.2, True)
print(my_tuple[0]) #output: 1
print(type(my_tuple) )  #output: <class 'tuple'>
print(my_tuple.count('Owais')) #output: 1
print(my_tuple.index("Owais")) #output: 1

```


## Set
An unordered collection of unique elements, Set are mutable. Sets are often used to represent mathematical sets, but they can also be used for other purposes.

```
list = [1,2,3,4,5,6]
my_set = set(list)
print(my_set) #output: {1,2,3,4,5,6}

set = {4,5,6,6,7,7,8,9}
print(set) #output: {4,5,6,7,8,9}
```

**Sets with built-in method**
Sets in python come up with several built-in method that allow you to perform various operations on sets.


1. **add()**: Adds an element to the set.
```
my_set = {1,2,3,4,5,6}
set = {4,5,6,6,7,7,8,9}
my_set.add(10)
print(my_set) #output: {1, 2, 3, 4, 5, 6, 10}
```


2. **remove()**: Removes the specified element from the sets.
```
my_set = {1,2,3,4,5,6}
set = {4,5,6,6,7,7,8,9}
my_set.remove(4) 
print(my_set) #output: {1, 2, 3, 5, 6}
```


3. **discard()**: Removes the specified element from the set if exists.
```
my_set = {1,2,3,4,5,6}
set = {4,5,6,6,7,7,8,9}
my_set.discard(1)
print(my_set) #output: {2, 3, 4, 5, 6}
```


4. **union()** Returns a new set that contains all the elements from both the original set and another set.
```
my_set = {1,2,3,4,5,6}
set = {4,5,6,6,7,7,8,9}
print(my_set.union(set)) #output: {1, 2, 3, 4, 5, 6, 7, 8, 9}
print(my_set|set) #output: {1, 2, 3, 4, 5, 6, 7, 8, 9}
```


5. **intersection()** Returns a new set that contains elements common to both the original set and another set.
```
my_set = {1,2,3,4,5,6}
set = {4,5,6,6,7,7,8,9}
print(my_set.intersection(set)) #output: {4, 5, 6}
print(my_set & set ) #output: {4, 5, 6}
```


6. **difference()** Return a new set that contains elements from the original set that are not in the other set.
```
my_set = {1,2,3,4,5,6}
set = {4,5,6,6,7,7,8,9}
print(my_set.difference(set)) #output: {1, 2, 3}
print(my_set-set) #output: {1, 2, 3}
```


7. **symmetric_difference()** Returns a set that contains all items from both set, but not the items that are present in both set.
```
my_set = {1,2,3,4,5,6}
set = {4,5,6,6,7,7,8,9}
print(my_set.symmetric_difference(set)) #output: {1, 2, 3, 7, 8, 9}
print(my_set^set) #output: {1, 2, 3, 7, 8, 9}
```

## Dictionary
A dictionary is a collection of key-value pairs. The keys are unique, and the values can be of any data type. Dictionaries are mutable, which means that they can be changed.

```
my_dict = {1:'Owais', 2:'Jason', 3:'Jackob'}
print(my_dict)

del my_dict[2]
print(my_dict)

my_dict[2] = 'Ali'
print(my_dict)

for x,y in my_dict.items():
    print(str(x)+': '+y)
```


## Args
Args is special variable in python that is used to pass a variable number of arguments to a function. When you define a function, you can use the _*args_ syntax to indicate that the function can take a variable number of arguments.

```
def sum_of(*args):
    sum = 0
    for x in args:
        sum += x
    return sum

print(sum_of(2,3,4,5,6,7)) #output: 27
```


## Kwargs
Kwargs is a special variable that is used to pass a variable number of keyword arguments to a function. When you define a function, you can use _**kwargs_ syntax to indicate that the function can take a variable number of keyword arguments.

```
def key_word(**kwargs):
    for x,y in kwargs.items():
        sum = 0
        for x,y in kwargs.items():
            sum += y
        return round(sum,2)
    
print(key_word(coffee=2.5, Tea=4.55, Water=6.88))

```
