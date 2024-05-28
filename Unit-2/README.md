<h2 align="center">Unit - 2</h2>
<h2 align="center">Python  Program  Flow  Control  Conditional  Block</h2>

## Python if Statement
An if statement executes a block of code only if the specified condition is met.

#### Syntax
```py
if condition:
    # body of if statement
```
Here, if the condition of the if statement is:
- **True** - the body of the if statement executes.
- **False** - the body of the if statement is skipped from execution.

#### Code 
```py
number = 10

# check if number is greater than 0
if number > 0:
    print('Number is positive')

print('This statement always executes')
```
#### Output
````py
Number is positive
This statement always executes
````



## Python if...else Statement
An if statement can have an optional else clause. The else statement executes if the condition in the if statement evaluates to False.

#### Syntax
```py
if condition:
    # body of if statement
else:
    # body of else statement
```
Here, if the condition inside the if statement evaluates to
- **True** - the body of if executes, and the body of else is skipped.
- **False** - the body of else executes, and the body of if is skipped

#### Code 
```py
number = 10

if number > 0:
    print('Positive number')
else:
    print('Negative number')

print('This statement always executes')
```
#### Output
````py
Positive Number
This statement is always executed
````



## Python if…elif…else Statement
The if...else statement is used to execute a block of code among two alternatives.
However, if we need to make a choice between more than two alternatives, we use the if...elif...else statement.

#### Syntax
```py
if condition1:
    # code block 1

elif condition2:
    # code block 2

else: 
    # code block 3
```

Here,
- **if condition1** - This checks if condition1 is True. If it is, the program executes code block 1.
- **elif condition2** - If condition1 is not True, the program checks condition2. If condition2 is True, it executes code block 2.
- **else** - If neither condition1 nor condition2 is True, the program defaults to executing code block 3.

#### Code 
```py
number = 0
if number > 0:
    print('Positive number')
elif number <0:
    print('Negative number')
else:
    print('Zero')
print('This statement is always executed')
```
#### Output
````py
Zero
This statement is always executed
````
