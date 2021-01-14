#### General
````
echo                # output one or more strings
print               # output a string
unset               # unset a given variable
isset               # determine if a variable is set and is not NULL
empty               # determine whether a variable is empty
include             # include and evaluate the specified file
require             # include and evaluate the specified file, raise CompileError upon failure
die                 # output a message and terminate the current script
````
#### String
````
strlen()            # returns string length
substr()            # return part of a string
strpos()            # position of first occurrence of case insensitive substring
strtolower()        # make string lowercase
strtoupper()        # make string uppercase
strrev()            # reverse a string
str_split()         # convert a string to array
strcmp()            # binary safe string comparison
strtr()             # translate characters or replace substrings
str_replace()       # replaces some characters with some other characters in a string
trim()               # removes the white-spaces from both start and the end of the string
ltrim()              # removes the white-spaces from the left part of the string
rtrim()              # removes the white-spaces from the right part of the string
explode()            # breaks the string into array on the basis of delimiter passed
implode()            # join array elements with a string on the basis of delimiter passed
````
#### Array
````
count($array)                     # count all elements in array
array_values($array)              # retrieve all the values from an associative array
array_keys($array)                 # retrieve all the keys from an associative array
array_diff($array)                # values present in first argument but not in other arguments
array_intersect($array)           # values present in first argument and in other arguments
array_merge($array)               # merge one or more arrays in the first argument
array_pop($array)                 # pop the element off the end of array
array_push($array, $value)        # push one or more elements onto the end of array
array_shift($array)               # removes an element from the beginning of an array
array_unshift($array, $value)     # adds an element to the beginning of an array
array_reverse($array)             # reverse array elements
array_flip($array)                # flipped array on success else null
array_search($needle, $array)     # searches for needle in array and returns key
in_array($searched_value, $array) # searches an array for a specific value
array_key_exists($key, $array)    # returns TRUE if the given key is set in the array
sort($array)                      # sort arrays in ascending order
rsort($array)                     # sort arrays in descending order
asort($array)                     # sort associative arrays in ascending order, according to the value
ksort($array)                     # Sort associative arrays in ascending order, according to the key
arsort($array)                    # sort associative arrays in descending order, according to the value
krsort($array)                    # sort associative arrays in descending order, according to the key
````
#### File
````
fopen()                           # opens a file or url
fclose()                          # closes an open file pointer
fread()                           # reads bytes from file pointer
fgets()                           # reads line from file pointer
fwrite()                          # writes bytes to a file pointer
file_exists()                     # checks whether a file or directory exists
Date/Time
date()                            # formats a local time/date
time()                            # returns the current Unix timestamp
mktime()                          # get Unix timestamp from a date
microtime()                       # returns the current Unix timestamp with microseconds
````
