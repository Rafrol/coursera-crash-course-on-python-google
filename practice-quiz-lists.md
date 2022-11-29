# Practice Quiz: Lists

## Question 1
Given a list of filenames, we want to rename all the files with extension hpp to the extension h. To do this, we would like to generate a new list called newfilenames, consisting of the new filenames. Fill in the blanks in the code using any of the methods you’ve learned thus far, like a for loop or a list comprehension.

```
filenames = ["program.c", "stdio.hpp", "sample.hpp", "a.out", "math.hpp", "hpp.out"]
# Generate newfilenames as a list containing the new filenames
# using as many lines of code as your chosen method requires.
___  

print(newfilenames) 
# Should be ["program.c", "stdio.h", "sample.h", "a.out", "math.h", "hpp.out"]
```

Answer:
```
filenames = ["program.c", "stdio.hpp", "sample.hpp", "a.out", "math.hpp", "hpp.out"]
# Generate newfilenames as a list containing the new filenames
# using as many lines of code as your chosen method requires.
newfilenames = []
for files in filenames:
    if files.endswith("hpp"):
        newfiles = files.replace("hpp","h")
        newfilenames.append(newfiles)
        
    else:
        newfilenames.append(files)
        

print(newfilenames) 
# Should be ["program.c", "stdio.h", "sample.h", "a.out", "math.h", "hpp.out"]
```

Another answer:

```
filenames = ["program.c", "stdio.hpp", "sample.hpp", "a.out", "math.hpp", "hpp.out"]
# Generate newfilenames as a list containing the new filenames
# using as many lines of code as your chosen method requires.
newfilenames = [file.replace('.hpp', '.h') for file in filenames]

print(newfilenames)
# Should be ["program.c", "stdio.h", "sample.h", "a.out", "math.h", "hpp.out"]
```

***
## Question 2
Let’s create a function that turns text into pig latin: a simple text transformation that modifies each word moving the first character to the end and appending “ay” to the end. For example, python ends up as ythonpay.

```
def pig_latin(text):
  say = ""
  # Separate the text into words
  words = ___
  for word in words:
    # Create the pig latin word and add it to the list
    ___
    # Turn the list back into a phrase
  return ___
		
print(pig_latin("hello how are you")) # Should be "ellohay owhay reaay ouyay"
print(pig_latin("programming in python is fun")) # Should be "rogrammingpay niay ythonpay siay unfay"
```
Answer:
```
def pig_latin(text):
  say = []
  # Separate the text into words
  words = text.split()
  for word in words:
    # Create the pig latin word and add it to the list
    newword = str(word[1:]) + str(word[0]) + "ay"
    say.append(newword)

    # Turn the list back into a phrase
  return " ".join(say)
```

Another answer:
```
def pig_latin(text):
  say = ""
  # Separate the text into words
  words = text.split()
  for word in words:
    # Create the pig latin word and add it to the list
    pig_latin_word = word[1:] + word[0] + 'ay'
    say += ' ' + pig_latin_word
    # Turn the list back into a phrase
  return say

print(pig_latin("hello how are you")) # Should be "ellohay owhay reaay ouyay"
print(pig_latin("programming in python is fun")) # Should be "rogrammingpay niay ythonpay siay unfay"
```
***
## Question 3
The permissions of a file in a Linux system are split into three sets of three permissions: read, write, and execute for the owner, group, and others. Each of the three values can be expressed as an octal number summing each permission, with 4 corresponding to read, 2 to write, and 1 to execute. Or it can be written with a string using the letters r, w, and x or – when the permission is not granted. For example: 640 is read/write for the owner, read for the group, and no permissions for the others; converted to a string, it would be: “rw-r—–” 755 is read/write/execute for the owner, and read/execute for group and others; converted to a string, it would be: “rwxr-xr-x” Fill in the blanks to make the code convert a permission in octal format into a string format.

```
def octal_to_string(octal):
    result = ""
    value_letters = [(4,"r"),(2,"w"),(1,"x")]
    # Iterate over each of the digits in octal
    for ___ in [int(n) for n in str(octal)]:
        # Check for each of the permissions values
        for value, letter in value_letters:
            if ___ >= value:
                result += ___
                ___ -= value
            else:
                ___
    return result
    
print(octal_to_string(755)) # Should be rwxr-xr-x
print(octal_to_string(644)) # Should be rw-r--r--
print(octal_to_string(750)) # Should be rwxr-x---
print(octal_to_string(600)) # Should be rw-------
```
Answer:
```
def octal_to_string(octal):
    result = ""
    value_letters = [(4,"r"),(2,"w"),(1,"x")]
    # Iterate over each of the digits in octal
    for digit in [int(n) for n in str(octal)]:
        # Check for each of the permissions values
        for value, letter in value_letters:
            if digit >= value:
                result += letter
                digit -= value
            else:
                result += '-'
    return result

print(octal_to_string(755)) # Should be rwxr-xr-x
print(octal_to_string(644)) # Should be rw-r--r--
print(octal_to_string(750)) # Should be rwxr-x---
print(octal_to_string(600)) # Should be rw-------
```
***
## Question 4
Tuples and lists are very similar types of sequences. What is the main thing that makes a tuple different from a list?

A tuple is mutable&nbsp;  
A tuple contains only numeric characters&nbsp;  
_**A tuple is immutable**_&nbsp;  
A tuple can contain only one type of data at a time&nbsp;  
***
## Question 5
The group_list function accepts a group name and a list of members, and returns a string with the format: group_name: member1, member2, … For example, group_list(“g”, [“a”,”b”,”c”]) returns “g: a, b, c”. Fill in the gaps in this function to do that.

```
def group_list(group, users):
  members = ___
  return ___

print(group_list("Marketing", ["Mike", "Karen", "Jake", "Tasha"])) # Should be "Marketing: Mike, Karen, Jake, Tasha"
print(group_list("Engineering", ["Kim", "Jay", "Tom"])) # Should be "Engineering: Kim, Jay, Tom"
print(group_list("Users", "")) # Should be "Users:"
```

Answer:
```
def group_list(group, users):
  return "{}: {}".format(group, ", ".join(users))

print(group_list("Marketing", ["Mike", "Karen", "Jake", "Tasha"])) # Should be "Marketing: Mike, Karen, Jake, Tasha"
print(group_list("Engineering", ["Kim", "Jay", "Tom"])) # Should be "Engineering: Kim, Jay, Tom"
print(group_list("Users", "")) # Should be "Users:"
```

Another answer:
```
def group_list(group, users):
  members = ', '.join(users)
  return '{}:{}'.format(group, ' ' + members)

print(group_list("Marketing", ["Mike", "Karen", "Jake", "Tasha"])) # Should be "Marketing: Mike, Karen, Jake, Tasha"
print(group_list("Engineering", ["Kim", "Jay", "Tom"])) # Should be "Engineering: Kim, Jay, Tom"
print(group_list("Users", "")) # Should be "Users:"
```
***
## Question 6
The guest_list function reads in a list of tuples with the name, age, and profession of each party guest, and prints the sentence “Guest is X years old and works as __.” for each one. For example, guest_list((‘Ken’, 30, “Chef”), (“Pat”, 35, ‘Lawyer’), (‘Amanda’, 25, “Engineer”)) should print out: Ken is 30 years old and works as Chef. Pat is 35 years old and works as Lawyer. Amanda is 25 years old and works as Engineer. Fill in the gaps in this function to do that.

```
def guest_list(guests):
	for ___:
		___
		print(___.format(___))

guest_list([('Ken', 30, "Chef"), ("Pat", 35, 'Lawyer'), ('Amanda', 25, "Engineer")])

#Click Run to submit code
"""
Output should match:
Ken is 30 years old and works as Chef
Pat is 35 years old and works as Lawyer
Amanda is 25 years old and works as Engineer
"""
```
Answer:
```
def guest_list(guests):
	for guest, age, profession in guests:
		print("{} is {} years old and works as {}".format(guest, age, profession))

guest_list([('Ken', 30, "Chef"), ("Pat", 35, 'Lawyer'), ('Amanda', 25, "Engineer")])

#Click Run to submit code
"""
Output should match:
Ken is 30 years old and works as Chef
Pat is 35 years old and works as Lawyer
Amanda is 25 years old and works as Engineer
"""
```

Another answer:
```
def guest_list(guests):
    for person in guests:
        name, age, profession = person
        print('{} is {} years old and works as {}'.format(name, age, profession))


guest_list([('Ken', 30, "Chef"), ("Pat", 35, 'Lawyer'), ('Amanda', 25, "Engineer")])

"""
Output should match:
Ken is 30 years old and works as Chef
Pat is 35 years old and works as Lawyer
Amanda is 25 years old and works as Engineer
"""
```