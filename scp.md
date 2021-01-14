### GENERAL
#### Usage
````
scp <options> <source_path> <destination_path>
````

#### Options
````
-r      # transfer directory
-v      # see the transfer details
-C      # copy files with compression
-l 800  # limit bandwith with 800
-p      # preserving the original attributes of the copied files
-q      # hidden the output
````

#### Commands
````
scp file user@host:/path/to/file
scp user@host:/path/to/file /local/path/to/file
scp file1 file2 user@host:/path/to/directory
scp -r /path/to/directory user@host:/path/to/directory
````
