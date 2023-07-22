# Introduction to Python Programming
## Definition
**Programming**
Programming is the process of giving a computer a specific set of instructions in a particular language that it can comprehend and execute, enabling it to perform a desired operation or task.


**Python**
Python is a general-purpose, high-level programming language.  Its design philosophy emphasizes code readability with the use of significant indentation. Its language constructs object-oriented approach aims to help programmers write clear, logical code for small and large scale of projects.


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
A variable is a named location in memory that stores a value. Variable are used to store data that needs to be used throughout a program.

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
**print()**
Display the value passed to it.
```
print(‘hello world’) # output : hello world
```


**input()**
Used to get input from the user.
```
name = input(‘what is your name? ’)
prints(name) # output: display the value which was entered by the user.
```


## Type casting:
**Process of converting one data type to another. Python has to types of conversion:**

**Implicit:** When the python interpreter automatically converts a value from one data type to another. 


**Explicit:** When you explicitly convert a value from one data type to another by using built in function.

1. **str():** Converts a number or float into string.
2. **int():** Converts a string or float into the integer.
3. **float():** Converts a string or integer into the float.
4. **ord():** Returns the Unicode point of the character.
5. **hex():** Returns the hexadecimal representation of a character.
6. **oct():** Returns the octal representation of a number.
7. **tuple():** Creates a tuple.
8. **set():** Creates a set.
9. **list():** Creates a list.
10. **dict():** Creates a dictionary. 


**str()**
Convert the provided value into a string.
```
str(55) # The integer value 55 will be converted into the string.
```


**int()**
Convert the provided value into the integer.
```
int(‘555’) # string value will be converted into the integer.
```

**len()**
Return the length of an object.

```
print(len(‘hello’) # output: 5
```


**float()**
This function can be used to covert the provided value into the float.
```
Number = 12
print(float(Number)) #output: 12.0
```


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

## User Input and Console Output:
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




