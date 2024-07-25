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
file = open("example.txt","r")


```


