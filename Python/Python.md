### Python Programming Language
--------------------------------------
* Python is a High level, interpreted programing language that is used for variety of application, including web development, scientific computing, data analysis, machine learning and artificial intelligence. This language was first released in 1991 by Guido Van Rossum.
--------------------------------------
* Replit: An online development environment that allow developers to write, test, and deploy code in web browser.
* Modules:  A pythons file containing Python definition and statements.
* There are two types of Modules:
  - Built-in Modules: These are the part of Python standard library and are available for use without any additional installation.
  - User-Defined Modules: These are created by the user to perform a specific task or set of tasks.
* Python Package Index (PIP): A package manager that allow developers to easily download, install and manage external modules and packages.
* Some PIP Commands are as following:
  - pip list: Show a list of all installed packages and their versions.
  - pip show package_name: Display information about specific package.
  - pip install --upgrade package_name: Upgrade a package to the latest version.
  - pip uninstall package_name: Uninstall a package. 

* ‘print()’: Display output on the console or in a file.
	> print(“Hello World”)
* Comments: Add explanatory and informative text to a program’s source code.
  - Single line comment start with (#) :
	> #This is a single line comment (Short Key: Ctrl + /)
  - Multiple line comment are enclosed with triple quotes (“””):
	> ””” This is a multiple-line comment
	> that spans multiple lines”””
* Escape Sequence Character (Back Slash: \): To insert characters that cannot be directly used in a string, we use an escape sequence character. 
	> print("This will \"execute\"")
* sep=: Allow you to specify a separator between the values you are printing.
	> print("Harry", "Jerry", "Merry", sep=", ")
* end=: Specify what to print at the end.
	> print("Harry", "Jerry", "Merry", end=" Thanks")
* Variable: A container that hold data.
	> name = “Owais” 
* Data type: Specifies the type of value a variable hold.
  - int: 3, -8, 0
  - float: 7.347, -9.0, 0.0001
  - complex: 6 + 2i
  - str: “Hello world” (A text data type)
	> print(“Hello World”)
  - Boolean: Consist of values True and False.
  - list: An ordered collection of data with element separated by commas and enclosed with square brackets.
	> list1 = [8, 2.3, [-4, 5], [“apple”, “banana”]]
  - tuple(): Similar to a list but this is immutable.
  - dict: Data structure that allows for efficient lookup, insertion, and deletion of key value pair.
	> my_dict = {“apple”: 2, “banana”: 3, “orange”: 5}
  - type(): Determine the data type of a given object.
	> print(type(name))

* Operators: Python has different type operators which perform operations.
* Arithmetic Operators: 
  - Addition (+)
  - Subtraction (-) 
  - Multiplication (*) 
  - Exponential (**) 
  - Division (/)
  - Modulus (%)
  - Floor Division (//)

* Typecasting: Conversion of one data type into another data type, there are two types of typecasting:
- Explicit: Conversion of one data type into another type manually. _(int(), str(), oct(), float(), and hex())_
- Implicit: Automatically convert a data type into another data type. _(type())_

* input(): Allow user to enter a value or string from a command line or console.
	> Name = input(“Enter your name: “): This program will assign the value to the _Name_ variable. 

* **String:** Sequence of characters enclosed within either single quotes (‘…’) or double quotes (“…”).
	> name = “Owais” 
	
	> print(“Hello, ”+name)
	
	> print(‘He said, “I want to eat apple”.’)

* **Multilines Strings:** If our string has multiple line, we can create them like this:
	> a = """Lorem ipsum dolor sit amet,
	
	> consectetur adipiscing elit,
	
	> sed do eiusmod tempor incididunt
	
	> ut labore et dolore magna aliqua."""
	
	> print(a)

### String Methods
Python provide built-in methods that we can use to alter and modify strings.
* **upper():** Convert a string to upper case.
```
str1 = "AbcdEFGhi"
print(str1.upper())
```
* **lower():** Convert a string to lower case.
```
str1 = "AbcdEFGhi"
print(str1.lower())
```
* **strip():*** Remove any white spaces before and after the string.
```
str2 = " Silver Spoon "
print(str2.strip())
````
* **rstrip():** Remove any trailing charcters.
```
str3 = "Owais !!!"
print(str3.rstrip("!"))
```
* **replace():** Replace all occurrences of a string with another string.
```
str2 = "Silver Spoon"
print(str2.replace("Sp", "M"))
```
* **split():** Split the given string at the specified instance and return the separated string as list items.
```
str2 = "Silver Spoon"
print(str2.split(" "))
```
* **capitalize():** Turn only the first character of the string into upper case and other character to lower case.
```
str1 = "hello"
print(str1.capitalize())
str2 = "hello WorlD"
print(str2.capitalize())
```
* **center:** Aligns the string to the center as per parameter given by the user.
```
str1 = "Welcome to the console"
print(str1.center(50))
str1 = "Welcome to the console"
print(str1.center(50, "."))
```
* **count():** Return the number of times the given value has occurred with in the given string.
```
str2 = "Owais Hussain"
print(str2.count("s"))
```
* **endswith():** Check the string end with given value.
```
str2 = "Owais Hussain"
print(str2.endswith("is", 2, 5))
```
* **find():** Return the first occurrence of the of the given value and return the index where it is present.
```
str2 = "Owais Hussain is a good boy"
print(str2.find("is"))
```
* **index():** Return the first occurrence of the of the given value and return the index where it is present. If given value is absent from the string then raise and exception.
```
str2 = "Owais Hussain is a good boy"
print(str2.index("ishh"))
# Will show error
```
* **isalnum():** Return True only if the entire string only consist of A-Z, a-z, 0-9.
```
str1 = "WelcomBackToTheHome"
print(str1.isalnum())
```
* **isalpha():** Return True only if the entire string only consist of A-Z, a-z.
```
str1 = "WelcomBackToTheHome"
print(str1.isalpha())
```
* **islower():** Return True if all the character in the string are in lower case.
```
str1 = "owais"
print(str1.islower())
```
* **isprintable:** Return True if all values with in given string are printable.
```
str1 = "Osama Hussain playing cricket"
print(str1.isprintable())
```
* **isspace:** Return True, if the string contains white spaces.
```
str1 = "			" #Whether using spacebar or tab
print(str1.isspace())
```
* **istitle:** Return True, if the first letter of each string is capital.
```
str1 = "Owais Hussain Project"
print(str1.istitle())
```
* **isupper:** Return True, If all the characters in the string are in upper.
```
str1 = "WORLD HEALTH ORGANIZATION"
print(str1.isupper())
```
* **startswith():** Check the string starts with given value.
```
str1 = "Kisi Ka Bhai Kisi Ki Jan"
print(str1.startswith("Kisi"))
```
* **swapcase():** Changes the characters casing of the string.
```
str1 = "oWAIS hUSSAIN"
print(str1.swapcase())
```
* **title():** capitalizes each letter of the word within the string.
```
str1 = "honesty is the best policy"
print(str1.title())
```
