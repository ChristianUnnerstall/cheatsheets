### GENERAL
#### Usage
````
tar <options> <archive> <parameter>
````
#### Options
````
-c                                  # create a archive file.
-x                                  # extract a archive file.
-v                                  # show the progress of archive file.
-f                                  # filename of archive file.
-t                                  # viewing content of archive file.
-j                                  # filter archive through bzip2.
-z                                  # filter archive through gzip.
-r                                  # append or update files or directories to existing archive file.
-W                                  # Verify a archive file.
--wildcards                         # Specify patters in unix tar command.
````
#### Create tar archive
````
tar -cvf myArchive.tar /tmp/dir/
````
#### Create compressed tar.gz archive
````
tar -cvzf myCompressedArchive.tar.gz /tmp/dir/        # gz compression
tar -cvfj myCompressedArchive.tar.bz2 /tmp/dir/       # bz2 compression
````
#### Untar archive
````
tar -xvf myArchive.tar.gz
tar -xvf myArchive.tar.bz2
````
#### List archive content
````
tar -tvf myArchive.tar
````
#### Extract files from archive
````
tar -extract --file=myArchive.tar theFile.txt         # extract single file
tar -xvf myArchive.tar "theFile1.txt" "theFile2.log"  # extract multiple files
tar -xvf myArchive.tar --wildcards *.txt              # extract by wildcard
````
#### Add files or directories to archive
````
tar -rvf myArchive.tar newFile.txt                    # add file
tar -rvf myArchive.tar dir                            # add directory
````
