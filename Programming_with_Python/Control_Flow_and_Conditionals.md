# Control Flow and Conditionals

## Operators
A symbol that tells pythons to perform certain operations.


## Types of Operators

**Math Operators**
|Operator|Meaning|Example|
|------------|-----------|------------|
| +	     |Addition|2+3        	|
| -	     |Subtraction|3-2	|
| /	     |Division	|35/5	|
| *	     |Multiplication|3*5	|

```
print(5+4) # output: 9
print(5-2) #output: 3
print(35/5) #output: 7.0
print(5*7) #output: 35
```


**Logical operators**
|Operator	|Meaning	|Example	|
|--------------------|--------------------|--------------------|
| and 		|Checks for both conditions to be true		|4<5 and 5>3	|
| or 		| Checks for at least one condition to be true	|4<5 or 5>6	|
|not 		|Returns false if the condition is true		|not(4>5) or not(3>5)|

```
if 5>4 and 6<7:
    print('All values are True.') #output: All values are True.

if 5>4 or 5>6:
    print('Only first condition is True.') #output: Only first condition is True.

if  not(5>6) or not(5>6):
    print('Both conditions are False that is why this statement is printed.') #output: Both conditions are False that is why this statement is printed.
```


## Control Flow
Control flow refers to the order in which the instructions in program are executed.

**There are two types of control flows:**
**1. Condition Statements**
**if:** States that if the condition proves to True, a function is performed.
**else:** Catches anything which is not caught by the preceding conditions.
**elif:** Tests multiple conditions sequentially when the initial “if” condition evaluate to False.

```
 # Condition with if and elif statement.
name = input('Please enter name here: ')
age = int(input('Please enter your age.'))

if name == 'Owais':
    print(f'Hi {name}, I hope you are doing well.') # Hi Owais, I hope you are doing well.
elif age < 18:
    print('You are not eligible for this site.') # output: You are not eligible for this site.

 # Condition with else statement
name = input('Please enter name here: ')

if name == 'Owais':
    print(f'Hi {name}, I hope you are doing well.') # Hi Owais, I hope you are doing well.
else:
    print('Only registered users are allowed.') # output: Only registered users are allowed.
 
 # Complete condition with if, elif and else statement

billTotal = 95
discount1 = 10 
discount2 = 20 

if billTotal > 100 and billTotal<200:
  print('Bill is greter than 100.')
  billTotal = billTotal - discount1
elif billTotal > 200 and billTotal < 300:
  print('Bill is greater than 200.')
  billTotal = billTotal - discount2
else:
  print('Bill is less than 100.')

print(f'Total Bill: {billTotal}')

```


**2. Looping Construct**
A programming construct that allows you to execute a block of code repeatedly.


**Benefits of using looping construct:**
**Efficiency:** Used to automate tasks and process large amount of data.
**Readability:** Looping construct are very readable.
**Flexibility:** Used to iterate over any iterate able object.


**for** 
Checks for specific conditions and then repeatedly execute a block of code as long as those conditions are met.
```
employee = ['Owais', 'Osama', 'Hussain']

for name in range(len(employee)):
    print(employee[name])
```


**enumerate**
Used to iterate over a sequence and return both the index and value of each element in the sequence.
```
employee = ['Owais', 'Osama', 'Hussain']
for no, name in enumerate(employee):
    print(no+1, name)
```


**break** 
break statement in python is used to terminate a loop prematurely.
```
 #Starter Code
favorites = ['Creme Brulee', 'Apple Pie', 'Churros', 'Tiramisú', 'Chocolate Cake']

for dessert in favorites:
    if dessert == 'Pudding':
        print('Yes one of my favorite desserts is', dessert)
        break 
else:
    print('No sorry, not a dessert on my list')
```


**continue** 
Used to skip the rest of iteration of loop and continue with the next iteration.
```
 #Starter Code
favorites = ['Creme Brulee', 'Apple Pie', 'Churros', 'Tiramisú', 'Chocolate Cake']

for dessert in favorites:
    if dessert == 'Churros':
        continue
    print('Other desserts I like are', dessert)
```


**while** 
Repeat a specific block of code an unknown number of times until a condition is met.

```
while True:
    name = input('Please enter the name here: ')
    if name == 'Owais':
        print(f'Hi, {name}')
```


## Match statement
A match statement compares a value to several different conditions until one is met.


**match**
Starts by evaluating the value. If the value matches one of the patterns, then code block associated with that pattern is executed.


**case**
The case clauses in the match statement can be used to match any type of value.


**Benefits of using match statement:**
**1. Flexibility:** Used to match any type of value.
**2. Power:** Matches complex patters.
**3. Readability:** More readable than switch statement.

```
name = input()

match name:
    case 'Owais' | 'Osama' | 'Hussain':
        print(f'Glad to meet you {name}.')
    case 'Onaib' | 'Bilal':
        print(f'Long time no see {name}.')
    case _:
        print(f'Please register your name first {name}.')
```
