#### Navigation
````
ls                  # list directory contents
ls -alh             # formatted long listing with hidden files
cd <dir>            # change the current directory to the directory
cd ~                # change current directory to $HOME
cd /                # change the current directory to the root directory
cd ..               # change to the parent of the current directory
pwd                 # show name of current working directory
````

#### File Commands
````
mkdir -p <dir>                # create directory
rm <file>                     # remove file
rm -r <dir>                   # remove directory and its contents recursively
rm -f <file>                  # force remove file
rm -rf <dir>                  # recursively and forcefully remove a directory's contents
cp <file1> <file2>            # copy fil1 to file2
mv <file1> <file2>            # rename or move file1 to file2
ln -s <file> <link>           # create symbolic link to file
touch <file>                  # create file or change file timestamps
cmd > <file>                  # standard output (stdout) of cmd to file
cmd >> <file>                 # append stdout to file
cat <file1> <file2>           # concatenate file1 and file2 and print to stdout
less <file>                   # output the contents of the file 
more <file>                   # view contents of file one page at a time
head <file>                   # output first 10 lines of file
tail <file>                   # output last 10 lines of file
tail -f <file>                # output contents of file as it grows
sed -i 's,foo,bar,g' file.txt # replace instances of foo with bar
````

#### SSH
````
ssh <user>@<host>             # connect to host as user
ssh -p <port> <user>@<host>   # connect using port
ssh -D <port> <user>@<host>   # connect and use bind port
````
#### Network
````
ping <host>                   # ping host
whois <domain>                # get whois for domain
dig <domain>                  # get DNS for domain
dig -x host                   # Reverse lookup host
wget file                     # Download file
wget -c file                  # Continue stopped download
wget -r url                   # Recursively download files from url
````
