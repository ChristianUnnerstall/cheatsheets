#### HELP
````
help()              # enter the help mode
help(str)           # get help for 'str'
````
#### VARIABLES AND DATA TYPES
##### Variable Assignment
````
>>> x=13
>>> x
13
````
##### Calculation
````
x+2                   # Sum
x-2                   # Subtraction
x*2                   # Multiplication
x**2                  # Exponentiation
x%2                   # Remainder
x/float(2)            # Division
````
##### Types and Type Conversion
````
str()                # '13', '4.23', 'True'
int()                # 13, 6, 1
float()              # 13.0, 2.0
bool()               # True, False
````
##### Strings
````
>>> the_string = 'myAwesomeString'
>>> the_string
'myAwesomeString'
````
##### String Operations
````
>>> the_string * 2        
'myAwesomeStringmyAwesomeString'
>>> the_string + 'Yeah'
'myAwesomeStringYeah'
>>> 'n' in the_string
True
>>> the_string[5]
's'
>>> the_string[2:9]
'Awesome'
````
##### String Methods
````
the_string.upper()             # Uppercase
the_string.lower()             # Lowercase 
the_string.count('e')          # Count string 
the_string.replace('e', 'o')   # Replace string 
the_string.strip()             # Strip whitespaces
````
#### LISTS
##### Build
````
>>> a = 'is'
>>> b = 'awesome'
>>> the_list = ['this', 'list', a, b]
>>> the_list2 = [[2,3,4,5],[9,8,7,6]]
````
##### Selecting
````
>>> the_list[1]             # Select item at index 1
>>> the_list[-2]            # Select 2nd last item
>>> the_list[1:3]           # Select items at index 1 and 2
>>> the_list[2:]            # Select items after index 1
>>> the_list[:2]            # Select items before index 2
>>> the_list[:]
>>> the_list2[1][0]
>>> the_list2[1][:2]
````
##### Operations
````
>>> the_list + the_list
['this', 'list', 'is', 'awesome', 'this', 'list', 'is', 'awesome']
>>> the_list * 2       
['this', 'list', 'is', 'awesome', 'this', 'list', 'is', 'awesome']
````
##### Methods
````
the_list.index(a)          # Get the index of an item
the_list.count(a)          # Count an item 
the_list.append('!')       # Append an item at a time
the_list.remove('!')       # Remove an item 
del(the_list[0:1])         # Remove an item 
the_list.reverse()         # Reverse the list 
the_list.extend('!')       # Append an item 
the_list.pop(-1)           # Remove an item 
the_list.insert(0,'!')     # Insert an item
the_list.sort()            # Sort the list
````

#### SCRIPTS
````
$ touch hello.py
$ nano hello.py
````

````
!/usr/bin/python
print "Hello Python!"
````

````
$ chmod +x hello.py        # Set the executable flag
$ ./hello.py
````

#### LIBRARIES
##### Import libraries
````
import numpy
import numpy as np
````
##### Selective import
````
from math import pi
````

#### COMMENTS
````
# comment
````
print "Hello"     # another comment
...
  This is a multiline
  comment.
...
