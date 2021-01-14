### ITERATION
#### each
````
ul
    each val in [1, 2, 3, 4, 5]
        li= val
````
````
each
- var values = [];
````
````
ul
each val in values
    li= val
else
    li There are no values
````
### RENDER
#### JSON data
````
pre {{ data | json}}
````
