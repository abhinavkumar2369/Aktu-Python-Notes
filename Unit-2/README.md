<h2 align="center">Unit - 2</h2>
<h2 align="center">Python  Program  Flow  Control  Conditional  Block</h2>

## 🚀 Python if Statement
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
```
Number is positive
This statement always executes
```


<!-- ------------------------------------------------------------ -->


## 🚀 Python if...else Statement
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
```
Positive Number
This statement is always executed
```

<!-- ------------------------------------------------------------ -->


## 🚀 Python if…elif…else Statement
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

<!-- ------------------------------------------------------------ -->


## 🚀 Python for Loop

In Python, a for loop is used to iterate over sequences such as lists, strings, tuples, etc.

#### Syntax
```py
for val in sequence:
    # statement(s)
```
Here, val accesses each item of the sequence on each iteration. The loop continues until we reach the last item in the sequence.


### ➡️ For Loop in Lists
```py
languages = ['Swift', 'Python', 'Go']
```

#### Access elements of the list one by one
```py
for i in languages:
    print(i)
```

#### Output
```py
Swift
Python
Go
```

#### Explaination 
In the above example, we have created a list called languages. As the list has 3 elements, the loop iterates 3 times.
The value of i is --
1. Swift in the first iteration.  
2. Python in the second iteration.  
3. Go in the third iteration.  

<!-- ------------------------------------------------------------ -->


### ➡️ For Loop Through a String
```py
language = 'Python'
```

#### Iterate over each character in language
```py
for x in language:
    print(x)
```

#### Output
```
P
y
t
h
o
n
```
Here, we have printed each character of the string language using a for loop.


<!-- ------------------------------------------------------------ -->


### ➡️ For Loop with range()
In Python, the range() function returns a sequence of numbers. For example,

```py
values = range(4)
```
Here, range(4) returns a sequence of 0, 1, 2 ,and 3.  
Since the range() function returns a sequence of numbers, we can iterate over it using a for loop.



### Example(s) 
#### Iterate from i = 0 to i = 3

```py
for i in range(4):
    print(i)
```

#### Output

```
0
1
2
3
```


<!-- ------------------------------------------------------------ -->


## 🚀Note Python Range Function 
The Python `range()` function generates a sequence of numbers.  
By default, the sequence starts at 0, increments by 1, and stops **before** the specified number.

#### Syntax
`range(start, stop, step)`
The start and step arguments are optional.

#### Return Value
The `range()` function returns an immutable sequence of numbers.

<!-- ------------------------------------------------------------ -->

### ➡️ Example(s)

1. #### Create a sequence from 0 to 3
```py
numbers = range(4)
```

#### Iterating through the sequence
```py
for i in numbers:
    print(i)
```

#### Output
```
0
1
2
3
```

2. #### Iterate the loop five times
```py
for i in range(5):
    print(f'{i} Hello')
```

```
0 Hello
1 Hello
2 Hello
3 Hello
4 Hello
```


<!-- ------------------------------------------------------------ -->


### Other Formats -

### ➡️ `range(stop)`
- #### create a sequence from 0 to 3 (4 is not included)
```py
numbers = range(4)
```

- #### convert to list and print it
```py
print(list(numbers))    # Output: [0, 1, 2, 3]
```
In this example, we have converted the range sequence to a list.


### ➡️ `range(start, stop)`

- #### create a sequence from 2 to 4 (5 is not included)
```py
numbers = range(2, 5)
print(list(numbers))    # [2, 3, 4]
```

- #### create a sequence from -2 to 3
```py
numbers = range(-2, 4)    
print(list(numbers))    # [-2, -1, 0, 1, 2, 3]
```

- #### creates an empty sequence
```py
numbers = range(4, 2) 
print(list(numbers))    # []
```

### ➡️ `range(start, stop, step)`

- #### Create a sequence from 2 to 10 with increment of 3
```py
numbers = range(2, 10, 3)
print(list(numbers))    # [2, 5, 8]
```

- #### Create a sequence from 4 to -1 with increment of -1
```py
numbers = range(4, -1, -1)    
print(list(numbers))    # [4, 3, 2, 1, 0]
```

- #### range(0, 5, 1) is equivalent to range(5)
```py
numbers = range(0, 5, 1) 
print(list(numbers))    # [0, 1, 2, 3, 4]
```


 Use of while loops in python, 
Loop manipulation using pass, continue, break and else. 



<!-- ------------------------------------------------------------ -->

## 🚀 While Loop
In Python, we use the while loop to repeat a block of code until a certain condition is met.

### Syntax
```py
while condition:
    # body of while loop
```

### Example(s)

#### ➡️ Code
   
```py
number = 1

while number <= 3:
    print(number)
    number = number + 1
```

#### ➡️ Output

```
1
2
3
```

In the above example, we have used a while loop to print the numbers from 1 to 3. The loop runs as long as the condition number <= 3 is satisfied.

#### ➡️ Code

```py
# Calculate the sum of numbers until user enters 0
number = int(input('Enter a number: '))

total = 0

# iterate until the user enters 0
while number != 0:
    total += number
    number = int(input('Enter a number: '))

print('The sum is', total)
```

#### ➡️ Output
```
Enter a number: 3
Enter a number: 2
Enter a number: 1
Enter a number: -4
Enter a number: 0
The sum is 2
```

## 🚀 Infinite while Loop
If the condition of a while loop is always True, the loop runs for infinite times, forming an infinite while loop. For example,

```py
age = 32

# the test condition is always True
while age > 18:
    print('You can vote')
```

#### ➡️ Output
```
You can vote
You can vote
You can vote
.
.
.
```

`The above program is equivalent to:`

```py
age = 32
    
# the test condition is always True
while True:
    print('You can vote')
```


## 🚀 While loop with an else
In Python, a while loop can have an optional else clause - that is executed once the loop condition is False. For example,

#### ➡️ Code
```py
counter = 0

while counter  <  2:
    print('This is inside loop')
    counter = counter + 1
else:
    print('This is inside else block')
```

#### ➡️ Output
```
This is inside loop
This is inside loop
This is inside else block
```
Here, on the third iteration, the counter becomes 2 which terminates the loop. It then executes the else block and prints This is inside else block.

**Note**: The else block will not execute if the while loop is terminated by a break statement.


<!-- ------------------------------------------------------------ -->


## 🚀 Break & Continue Statement 
In programming, the break and continue statements are used to alter the flow of loops:
- break exits the loop entirely
- continue skips the current iteration and proceeds to the next one


### 🚀 Break
The break statement terminates the loop immediately when it's encountered.


#### ➡️ Syntax
```py
break
```


### 🚀 Break in For Loop
We can use the break statement with the for loop to terminate the loop when a certain condition is met.


#### Example
#### ➡️ Code
```py
for i in range(5):
    if i == 3:
        break
    print(i)
```

#### ➡️ Output
```
0
1
2
```


### 🚀 Break in While Loop
We can use a break statement inside a while loop to terminate the loop immediately without checking the test condition. For example,


#### ➡️ Code
```py
while True:
    user_input = input('Enter your name: ')

    # terminate the loop when user enters end
    if user_input == 'end':
        print(f'The loop is ended')
        break  

    print(f'Hi {user_input}')
```

#### ➡️ Output
```
Enter your name: Kevin
Hi Kevin
Enter your name: end
The loop is ended
```

Here, the condition of the while loop is always True. However, if the user enters end, the loop termiantes because of the break statement.


### 🚀 Python continue Statement
The continue statement skips the current iteration of the loop and the control flow of the program goes to the next iteration.

#### Syntax
```py
continue
```

<!-- ------------------------------------------------------------ -->


### Continue Statement with for Loop
We can use the continue statement with the for loop to skip the current iteration of the loop and jump to the next iteration. For example,

#### ➡️ Code
```py
for i in range(5):
    if i == 3:
        continue
    print(i)
```

#### ➡️ Output
```
0
1
2
4
```

In the above example,
```py
if i == 3:
    continue
```
skips the current iteration when i is equal to 3, and continues the next iteration. Hence, the output has all the values except 3.


<!-- ------------------------------------------------------------ -->


## 🚀 Pass Statement
- In Python programming, the pass statement is a null statement which can be used as a placeholder for future code.
- Suppose we have a loop or a function that is not implemented yet, but we want to implement it in the future. In such cases, we can use the pass statement.

#### ➡️ Syntax
```py
pass
```

#### ➡️ Example
```py
n = 10

# use pass inside if statement
if n > 10:
    pass

print('Hello')
```

#### Use of pass Statement inside Function or Class
We can do the same thing in an empty function or class as well. For example,
```py
def function(args):
    pass
class Example:
    pass
```
