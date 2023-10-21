# Functional Programming
Functional programming is a paradigm of building computer programs using expressions and functions without mutating state and data.


## Function
A function is a block of code that only executes when it is called. You can pass data, known as parameters, into a function. A function can return data as a result. It takes an input, processes it, and then produces a result.


## Pure Function

A pure function always returns the same result for same argument values and it has no side effect like modifying an argument or global variable.

 
**Differences between Pure and Traditional Function**

| Traditional Function           | Pure Function                  |
| -----------------------------  | ------------------------------  |
| Access global state            | Cannot access global state     |
| Modify global state            | Cannot modify global state     |
| Access local state             | Access local state             |
| Can change args                | Cannot change args             |
| Output does not depend on input | Output depends on input       |


## Benefits of Pure Function

1. **Predictable Outcome:** Pure functions always produce the same result for the same set of inputs, making their behavior highly predictable and reliable.
2. **Consistent Code:** Pure functions provide a consistent and reliable behavior, ensuring that they perform the intended tasks without unexpected side effects.
3. **Caching:** Because pure functions produce consistent results for the same inputs, they can be easily cached, optimizing performance in situations where the same computation is repeated with the same input values.
4. **Multi-threading:** Pure functions are well-suited for multi-threaded or concurrent programming environments because they don't rely on shared mutable state, reducing the risk of race conditions and making parallelization more manageable.



```
“””Example of Pure Function”””

myList = [1,2,3]

def add(lst, item):
    nl = lst.copy()
    nl.append(item)
    return nl

newList = add(myList, 7)
print(myList)
print(newList)

```

## Recursion

Recursion is programming technique where function call itself directly or indirectly to solve the problem.


```
“””Example No. 1”””
def countdown(n):
    print(n)
    if n == 0:
        return
    else:
        countdown(n-1) 

countdown(10)

“””” Example No. 2 ”””

def factorial(n):
    if n == 0:
        return 1
    else:
        return n*factorial(n-1)

print(factorial(5))

```

```
“”” Reversing a string in python “””
trial = 'reversal'
“”” Using slicing syntax [start:stop:step] with a step of -1 to reverse the string”””
new_trial = trial[::-1]
print(new_trial)

“”” Reversing string using recursive function ”””

def string_reverse(str):
    if len(str) == 0:
        return str
    else:
        return string_reverse(str[1:])+str[0]
    
str = "reversal"
reverse = string_reverse(str)
print(reverse)

```


## Map and Filter


**map()**: 
The map() function in Python is used to apply a specified function to each item in an input iterable (e.g., a list) and returns an iterator that produces the results. It takes two arguments: the first argument is the function to apply, and the second argument is the iterable containing the elements to be processed.


**filter()**:
The filter() function in Python is used to filter elements of an iterable (such as a list) based on a given function. It takes two arguments: the first argument is the function that defines the filtering condition, and the second argument is the iterable (e.g., a list) that contains the elements to be filtered.



```
“”” Define a list of employee names”””
data = ["Jackob", "Jason", "John", "Owais", "Ben", "Kelly", "Robert", "James"]

“”” Define a function called find_employee that takes an employee name as input “””
def find_employee(employee):
    “”” Check if the first letter of the employee's name is "J" “””
    if employee[0] == "J":
        “”” If the condition is true, return the employee's name “””
        return employee

“”” Use the map() function to apply the find_employee function to each element in the data list ”””
map_employee = map(find_employee, data)

print("USE OF MAP FUNCTION:")
print("---------------------------")
“”” Iterate through the map_employee object and print the results “””
for x in map_employee:
    print(x)



print("\n USE OF FILTER FUNCTION:")
print('------------------------------')
filter_employee = filter(find_employee, data)

for x in filter_employee:
    print(x)
```

