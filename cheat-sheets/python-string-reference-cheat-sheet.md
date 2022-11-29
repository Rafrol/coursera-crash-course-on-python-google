# String Reference Cheat Sheet

## String Reference Cheat Sheet
In Python, there are a lot of things you can do with strings. In this cheat sheet, you’ll find the most common string operations and string methods.

###  String operations

* **len(string)** - Returns the length of the string

* **for character in string** - Iterates over each character in the string

* **if substring in string** - Checks whether the substring is part of the string

* **string[i]** - Accesses the character at index **i** of the string, starting at zero

* **string[i:j]** - Accesses the substring starting at index **i**, ending at index **j** minus 1. If **i** is omitted, its value defaults to 0. If **j** is omitted, the value will default to **len(string)**.

### String methods
* **string.lower()** - Returns a copy of the string with all lowercase characters

* **string.upper()** - Returns a copy of the string with all uppercase characters

* **string.lstrip()** - Returns a copy of the string with the left-side whitespace removed

* **string.rstrip()** - Returns a copy of the string with the right-side whitespace removed

* **string.strip()** - Returns a copy of the string with both the left and right-side whitespace removed

* **string.count(substring)** - Returns the number of times substring is present in the string

* **string.isnumeric()** - Returns True if there are only numeric characters in the string. If not, returns False.

* **string.isalpha()** - Returns True if there are only alphabetic characters in the string. If not, returns False.

* **string.split()** - Returns a list of substrings that were separated by whitespace (whitespace can be a space, tab, or new line)

* **string.split(delimiter)** - Returns a list of substrings that were separated by whitespace or a delimiter

* **string.replace(old, new)** - Returns a new string where all occurrences of old have been replaced by new.

* **delimiter.join(list of strings)** - Returns a new string with all the strings joined by the delimiter 
