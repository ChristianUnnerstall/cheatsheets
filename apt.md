### apt-get
````
sudo apt-get update                 # updates package list
sudo apt-get upgrade                # installs new updated packages
sudo apt-get dist-upgrade           # smart upgrade to new packages
sudo apt-get install <package name> # installs package
sudo apt-get check                  # check for broken packages
sudo apt-get autoremove             # remove any orphaned packages
````
### apt-cache
````
apt-cache search <string>           # search name and description
apt-cache show <package>            # all the information on a package
apt-cache showpkg <package>         # all dependencies
apt-cache depends <package>         # what it depends on
apt-cache rdepends <package>        # what depends on it
````
### apt-file
````
sudo apt-get install apt-file       # needs to be installed
sudo apt-file update                # sync will all repositories 
apt-file search <string>            # searches for string, local and remote
apt-file list <package>             # list contents of package even if not installed
````
