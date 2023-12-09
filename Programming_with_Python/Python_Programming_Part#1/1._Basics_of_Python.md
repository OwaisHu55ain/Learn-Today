# Introduction to Python Programming
## Definitions
**Programming**

Programming is the process of instructing a computer to perform specific tasks or solve problems by providing it with a set of precise and logical instructions written in a programming language.


**Programming Language**

A programming language is a formal system of rules and syntax used to write and communicate instructions to a computer for the purpose of creating software and controlling its behavior.


**Python**

Python is a high-level, interpreted programming language known for its simplicity, readability, and versatility.


## Use of Python in Real Life
**Python is a popular programming language for variety of tasks, including:**
1. Data Science
2. Machine Learning
3. Artificial Intelligence
4. Software Development
5. System Administration
6. Scientific Computing
7. Scripting
8. Web Development


## Features
**Features of python**
1. Simple and Easy to Learn
2. Powerful
3. Extensible
5. Free and Open Source


## Variables
In Python, a variable is a symbolic name that represents a value or data stored in computer memory. It allows you to store and manipulate data within a program.


**Variable Name:** Sequence of letters, numbers and underscore that is used to identify a value in memory.

**Variable assignment:** Process of storing a value in a variable.

**Actual Value:** Refers to the value of a variable, expression or object.

```
name = 'Owais'
print(name) # output:  Owais

a = b = c = 10
print(a) # output: 10
print(b) # output: 10
print(c) # output: 10

a,b,c = 1,2,3
print(a) # output: 1
print(b) # output: 2
print(c) # output: 3

```

## Basic Data Types and Functions:

### Data Types
A data type is an attribute associated with a piece of data that tells the computer system how to interpret its value.


**Python data types are as following:**

1. **Numeric**
  	- **Integer:**  Whole number with no decimal places.
  	- **Float:** Contain decimal places.
  	- **Complex Number:** Made up of both real or imaginary numbers.
2. **Sequence**
  	- **String:** Sequence of characters that are enclosed either a single or double quotes.
  	- **List:** An array and hold any type inside the square brackets.
  	- **Tuples:** Same as list but they are immutable.
3. **Dictionary:** Store data in key value object structure.
4. **Boolean:** Simply represent as True and False.
5. **Set:** An unordered and non-indexed collection of non-repeated value.


**Data Types Examples**
|Data Type|Meaning|Example|
|-------|-------------|-----------|
|String|Text|’Hello’, ‘Testing 123’|
|Integer|Numbers|1,2,3,4,5|
|Float|Decimal|2.3,4.3,5.6|


## Flow Control
Flow control refers to the mechanisms and constructs used to control the order in which statements and instructions are executed in a program.


**Comparison Operator:** A comparison operator is a type of operator in programming that allows you to compare two values or variables.

|Operator|Meaning|Example|
|------------|-----------|------------|
|==|Equal|A==A|
|!=|Not Equal | A != B|
|<|Less Than|A<B|
|>|Greater Than |A>B|
|<=|Less Than Or Equal To| A<=|
|>= | Greater Than Or Equal To|A>=B|

```
a = 10.0
print(type(a)) # output: <class ‘float’>

b = 10
print(type(b)) # output: <class ‘int’>

c = ‘Owais’
print(type(c)) # output: <class ‘str’>

d = [1,2,3,4 ,5]
print(type(d)) #output: <class ‘list’>

```
```
variableA = "Hello world" # This is single line variable.
print(variableA) 

variableB = "This is too \n big to fit\n on a single line\n you multi-lined it." # this is multi line string.
print(variableB)

name = ‘Owais’
print(name) 
 #Reassigning a variable
name = ‘John’
print(name)
```


## Commenting Code
**Comments are helpful in following ways:**
1. Explaining what the code is intended to do.
2. Let developers knows that code is deprecated.
3. Add TODO comments for work to be completed.


**Types of Comments**
1. **Single Line Comment**
The use of # symbol tells python to ignore everything after this point until the end of the current line.
```
 # I’m a comment.
X = 10
```


2. **Multi Line Comments**
A multi line comment in python can be written using either triple single quotes (‘’’) or triple double quotes.
```
''' this is the multi line comment, 
using the single triple quotes'''

""" this is also a multi line comment,
Using the triple double quotes."""
```


3. **In Line Comments**
The # symbol tells the python to ignore everything after this point until the end of the current line.
```
X = 10 # This is in line comment.
```

## Built-in Functions:

Python comes with a rich set of built-in functions that provide essential functionality for a wide range of tasks. Here are some commonly used built-in functions in Python:


1. **`print()`**: Outputs text or variables to the console.

    ```python
    print("Hello, World!")
    ```

2. **`len()`**: Returns the length of an object (e.g., string, list, tuple).

    ```python
    my_list = [1, 2, 3, 4, 5]
    length = len(my_list)
    ```

3. **`type()`**: Returns the type of an object.

    ```python
    my_variable = 42
    variable_type = type(my_variable)
    ```

4. **`input()`**: Reads a line from the user input.

    ```python
    user_input = input("Enter something: ")
    ```

5. **`int()`, `float()`, `str()`**: Convert values to integer, float, or string types, respectively.

    ```python
    num_str = "42"
    num_int = int(num_str)
    ```

6. **`range()`**: Generates a sequence of numbers.

    ```python
    numbers = list(range(5))
    ```

7. **`max()`, `min()`**: Returns the maximum or minimum value from a sequence.

    ```python
    numbers = [2, 5, 1, 8, 3]
    max_value = max(numbers)
    ```

8. **`sum()`**: Returns the sum of all elements in a sequence.

    ```python
    numbers = [1, 2, 3, 4, 5]
    total = sum(numbers)
    ```

9. **`sorted()`**: Returns a sorted version of a list, tuple, or string.

    ```python
    my_list = [3, 1, 4, 1, 5, 9, 2]
    sorted_list = sorted(my_list)
    ```

10. **`abs()`**: Returns the absolute value of a number.

    ```python
    absolute_value = abs(-42)
    ```

11. **`round()`**: Rounds a floating-point number to the nearest integer.

    ```python
    rounded_number = round(3.14159, 2)
    ```

These are just a few examples of the many built-in functions available in Python. The Python documentation is an excellent resource for exploring the full list and details of these functions: [Python Built-in Functions](https://docs.python.org/3/library/functions.html).



## Type casting:
In programming, type casting refers to converting a variable from one data type to another. Type casting can be broadly categorized into two types: implicit (automatic) type casting and explicit (manual) type casting.

### Implicit (Automatic) Type Casting:

Implicit type casting, also known as automatic type conversion, occurs automatically when the interpreter handles the conversion without any explicit instructions from the programmer. This typically happens when the destination data type can accommodate the values of the source data type without loss of information.

Here's an example in Python:

```python
num_int = 42
num_float = 3.14

result = num_int + num_float
```

In this example, `num_int` (an integer) is implicitly converted to a float before the addition operation, so that the result is a float.

### Explicit (Manual) Type Casting:

Explicit type casting, also known as manual type conversion, occurs when the programmer specifically instructs the interpreter to perform the type conversion. This is done using built-in functions that are designed for type casting.

Here's an example in Python:

```python
num_str = "42"
num_int = int(num_str)
```

In this example, the `int()` function is used for explicit type casting, converting the string `"42"` to an integer.

### Examples in Python:

#### Implicit Type Casting:

```python
num_int = 42
num_float = 3.14

result = num_int + num_float
print(result)  # Output: 45.14
```

#### Explicit Type Casting:

```python
num_str = "42"
num_int = int(num_str)

print(num_int)  # Output: 42
```


Here are some commonly used ones:

1. **`int()`**: Converts a number or a string containing a whole number to an integer.

    ```python
    num_str = "42"
    num_int = int(num_str)
    ```

2. **`float()`**: Converts a number or a string containing a number (integer or floating-point) to a floating-point number.

    ```python
    num_str = "3.14"
    num_float = float(num_str)
    ```

3. **`str()`**: Converts an object to a string.

    ```python
    number = 42
    num_str = str(number)
    ```

4. **`bool()`**: Converts an object to a Boolean value. In general, any object is considered `True` unless it's empty, `0`, or `None`.

    ```python
    value = 0
    bool_value = bool(value)
    ```

5. **`list()`, `tuple()`, `set()`**: Converts an iterable (e.g., a string, tuple, or dictionary) to a list, tuple, or set, respectively.

    ```python
    my_string = "hello"
    list_from_string = list(my_string)
    ```

6. **`dict()`**: Converts a sequence of key-value pairs to a dictionary.

    ```python
    key_value_pairs = [('a', 1), ('b', 2), ('c', 3)]
    my_dict = dict(key_value_pairs)
    ```

7. **`set()`**: Converts an iterable to a set.

    ```python
    my_list = [1, 2, 3, 1, 2, 3]
    my_set = set(my_list)
    ```

8. **`ord()`**, **`chr()`**: `ord()` returns an integer representing the Unicode character, and `chr()` converts an integer to its corresponding Unicode character.

    ```python
    unicode_char = 'A'
    unicode_int = ord(unicode_char)
    ```

    ```python
    unicode_int = 65
    unicode_char = chr(unicode_int)
    ```

These functions help you convert between different data types in Python. Keep in mind that not all conversions are possible or meaningful, so it's essential to choose the appropriate type casting based on your specific requirements.

**String Concatenation**
Joining two or more string together to create a new string.

```
str1 = ‘hello’
str2 = ‘world’
print(str1+str2) # output: hello world
```


**Index**
A position with in a sequence.
```
name = ‘owais’
print(name[0]) #output: o
print(name[1]) #output: w
print(name[2]) #output: a
print(name[3]) #output: i
print(name[4]) #output: s
```

## Creating Function
Python function is a block of code that is executed when it is called.  To create a function in Python you use the **def** keyword.

```
def greeting(name):
    print('Hello '+name+' !')
greeting('Owais') #output : Hello Owais !

def greeting(name):
    return 'Hello '+name+' !'
print(greeting('Owais'))
```

## User Input and Console Output

User input is the data that is entered by the user, while console output is the data that is displayed by the console.


**sep=**
Used to specify the separator.
```
print(1,2,3, sep=', ')

```


**end=**
It specifies the string that should be appended at the end of printed output.
```
print('hello'.title(), end=' ')
print('world'.title(), end='!')
```




