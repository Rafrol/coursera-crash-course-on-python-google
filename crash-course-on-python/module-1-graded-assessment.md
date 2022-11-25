# Module 1 Graded Assessment

## Question 1

What is a computer program?

A file that gets printed by the Python interpreter.&nbsp;  
The syntax and semantics of Python.&nbsp;  
The overview of what the computer will have to do to solve some automation problem.&nbsp;  
_**A step-by-step recipe of what needs to be done to complete a task, that gets executed by the computer.**_&nbsp;  

***
## Question 2

What's automation?

The inputs and outputs of a program.&nbsp;  
_**The process of replacing a manual step with one that happens automatically.**_&nbsp;  
The checkout processes at a grocery store.&nbsp;  
The process of getting a haircut.&nbsp;  
***
## Question 3

Which of the following tasks are good candidates for automation? Check all that apply.

Writing a computer program.&nbsp;  
_**Creating a report of how much each sales person has sold in the last month.**_&nbsp;  
_**Setting the home directory and access permissions for new employees joining your company.**_&nbsp;  
Designing the new webpage for your company.&nbsp;  
Taking pictures of friends and family at a wedding.&nbsp;  
_**Populating your company's e-commerce site with the latest products in the catalog.**_&nbsp;  
***
## Question 4

What are some characteristics of the Python programming language? Check all that apply.

_**Python programs are easy to write and understand.**_&nbsp;  
_**The Python interpreter reads our code and transforms it into computer instructions.**_&nbsp;  
It's an outdated language that's barely in use anymore.&nbsp;  
_**We can practice Python using web interpreters or codepads as well as executing it locally.**_&nbsp;  
***
## Question 5

How does Python compare to other programming languages?

Python is the only programming language that is worth learning.&nbsp;  
_**Each programming language has its advantages and disadvantages.**_&nbsp;  
It's always better to use an OS specific language like Bash or Powershell than using a generic language like Python.&nbsp;  
Programming languages are so different that learning a second one is harder than learning the first one.&nbsp;  
***
## Question 6

Write a Python script that outputs "Automating with Python is fun!" to the screen.

Answer:
```
print("Automating with Python is fun!")
```
***
## Question 7

Fill in the blanks so that the code prints "Yellow is the color of sunshine".

```
color = ___
thing = ___
print(color + " is the color of " + thing)
```

Answer:
```
color = "Yellow"
thing = "sunshine"
print(color + " is the color of " + thing)
```
***
## Question 8

Keeping in mind there are 86400 seconds per day, write a program that calculates how many seconds there are in a week, if a week is 7 days. Print the result on the screen.
Note: Your result should be in the format of just a number, not a sentence.
```
x=86400*7
print(x)
```
***
## Question 9

Use Python to calculate how many different passwords can be formed with 6 lower case English letters. For a 1 letter password, there would be 26 possibilities. For a 2 letter password, each letter is independent of the other, so there would be 26 times 26 possibilities. Using this information, print the amount of possible passwords that can be formed with 6 letters
```
#Remind that in this case the letters can repeat, so we are talking about 26 possible letters for each 6 "blank spaces"

x=26**6
print(x)
```
***
## Question 10

Most hard drives are divided into sectors of 512 bytes each. Our disk has a size of 16 GB. Fill in the blank to calculate how many sectors the disk has.
Note: Your result should be in the format of just a number, not a sentence.
```
disk_size = 16*1024*1024*1024
sector_size = 512
sector_amount = ___
print(sector_amount)
```
Answer:
```
disk_size = 16*1024*1024*1024
sector_size = 512
sector_amount = disk_size/sector_size
print(sector_amount)
```