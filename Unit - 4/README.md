<h1 align="center">Unit - 4</h1>
<h1 align="center">Python File Operations</h1>





## 🚀 Reading files, Writing files
- Python provides built-in functions for creating, writing, and reading files.
- Two types of files can be handled in Python,
  1. Normal text files
  2. Binary files (written in binary language, 0s, and 1s).


### ➡️ Text files
- in this type of file, the data is stored in ASCII form or text form.
- Each line of text is terminated with a special character called EOL (End of Line), which is the new line character (‘\n’).

 
### ➡️ Binary files
- In this type of file, the data is stored in machine-understandable binary language (0's and 1's).
- They do not have any newline character at the end of any line (like '\n' in text files).






## 🚀 Reading Functions

### ➡️ Read()

- read() :
  
  This method read and return the entire the content of file in the form of string.

  
- read(n) :
  
  If n is specified, it will read only the n bytes.

#### Syntax --
- ```py
  with open('file.txt', 'r') as file:
    data = file.read()
    print(data)
  ```
- ```py
  file = open("example.txt","r")

  data = file.read()
  print(data)

  file.close()
  ```



### ➡️ Readline()

- readline() :

  Reads single line of the file & returns in form of a string.


- readlines(n) :

  If n given , reads at most n bytes, However, does not reads more than one line, even if n exceeds the length of the line.



### ➡️ Readlines()

- Reads all the lines and return them as each line as string element in a list.






## Example 🚀
Sample text file --> `example.txt` --->

```sh
Hello World\n
I am happy\n
Have a nice day
```

#### 1. Reading the entire file
```py
file = open("example.txt","r")

data = file.read()
# read() method wiil return the entire content of the file in form of string like this --->
# 'Hello World\nI am happy\nHave a nice day'

print(data)
```

#### Output --->
```sh
Hello World\n
I am happy\n
Have a nice day
```

![image](https://github.com/user-attachments/assets/94c70f77-49d1-44ba-b73d-2ad1c6170733)


#### 2. Reading a file line by line.
```py
#File Handler
file = open("example.txt","r")

# Reading Line by Line
# Strip() method remove newline character at each line
for line in file:
    print(line.strip())


# Closing the file
file.close()
```

#### Output --->
```sh
Hello World\n
I am happy\n
Have a nice day
```

![image](https://github.com/user-attachments/assets/1d1f0c08-0b71-4932-92bb-310552ba556e)

#### 3. Count the number of lines in file.
```py
# Opening File
file = open("example.txt",'r')

# Counting number of lines as file.readlines returns all line in form of list.
count = len(file.readlines())

print("The no. of lines is --->",count)

# Closing the files
file.close()
```
![image](https://github.com/user-attachments/assets/0e3ba070-6056-4508-aa6e-19e768f8b6ef)



#### 4. Copy Content from One File to Another.

```py
#  Date Copying
#  [01_example.txt]   ------->   [output.txt]


# Current File
file = open("01_example.txt",'r')

# Another File
output = open("output.txt",'w')

# Copying Data
output.write(file.read())


# File closing
file.close()
output.close()
```

![image](https://github.com/user-attachments/assets/616448b7-bbf1-4cf1-932b-1ea8d92a85a5)

```py
# Read from 'input.txt' and write to 'output.txt'
with open('input.txt', 'r') as file_in:
    with open('output.txt', 'w') as file_out:
        for line in file_in:
            file_out.write(line)
```



