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




## Different Modes
1. Read Mode (r)
  - Opens the file for reading. The file must exist.
  Syntax: `open('filename', 'r')`

  ```py
  with open('example.txt', 'r') as file:
      for line in file:
          print(line.strip())
  ```




2. Read and Write Mode (r+)
  - Opens the file for both reading and writing. The file must exist.
  Syntax: `open('filename', 'r+')`

  ```py
  with open('example.txt', 'r+') as file:
      content = file.read()
      file.write('New content')
  ```



3. Write Mode (w)
   
  - Opens the file for writing. If the file exists, it truncates (clears) the file. If the file does not exist, it creates a new file.
  Syntax: `open('filename', 'w')`
  ```py
  with open('example.txt', 'w') as file:
      file.write('Hello, world!')
  ```



4. Write and Read Mode (w+)
  - Opens the file for both writing and reading.
  - If the file exists, it truncates the file. If the file does not exist, it creates a new file.
  Syntax:  `open('filename', 'w+')`
  ```py
  with open('example.txt', 'w+') as file:
      file.write('Hello, world!')
      file.seek(0)
      content = file.read()
      print(content)
  ```



5. Append Mode (a)
   
  Opens the file for writing. If the file exists, it appends to the end of the file without truncating it. If the file does not exist, it creates a new file.
  Syntax: `open('filename', 'a')`
  ```py
  with open('example.txt', 'a') as file:
      file.write('Appending this line.')
  ```

6. Append and Read Mode (a+)
   
   Opens the file for both writing and reading. If the file exists, it appends to the end of the file without truncating it. If the file does not exist, it creates a new file.
    Syntax: open('filename', 'a+')
   ```py
    with open('example.txt', 'a+') as file:
        file.write('Appending this line.')
        file.seek(0)
        content = file.read()
        print(content)
    ```
   
## Binary Modes
These modes are used for binary files (like images or non-text files).

7. Read Binary Mode (rb)
- Opens the file for reading in binary mode. The file must exist.
  Syntax: `open('filename', 'rb')`
  ```py
  with open('example.png', 'rb') as file:
      content = file.read()
  ```

8. Write Binary Mode (wb)
- Opens the file for writing in binary mode. If the file exists, it truncates the file. If the file does not exist, it creates a new file.
  Syntax: `open('filename', 'wb')`
  ```py
  with open('example.png', 'wb') as file:
      file.write(b'binary data')
  ```


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



## 🚀 Writing Functions
There are two ways to write in a file.

1. write() :

   Inserts the string str1 in a single line in the text file.

   ```py
   file = open("output.txt","w")
   string = "1st Line\n 2nd Line\n 3rd Line"
   file.write(string)
   file.close()
   ```
   
![image](https://github.com/user-attachments/assets/7aa994e6-c0a5-4c3c-8c36-f9565c662e82)

   
2. writelines() :

   For a list of string elements, each string is inserted in the text file. Used to insert multiple strings at a single time.
   ```py
   file = open("output.txt","w")
   
   l = ["1st Line\n","2nd Line\n","3rd Line\n"]
   file.writelines(l)
   
   file.close()
   ```

![image](https://github.com/user-attachments/assets/20f1658b-956c-405c-a2b0-9e4901e9e1e6)



## Programs 🚀
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


#### Another method --->
```py
# Read from 'input.txt' and write to 'output.txt'

with open('input.txt', 'r') as file_in:
    with open('output.txt', 'w') as file_out:
        for line in file_in:
            file_out.write(line)
```



