#### HELP
````
git help <command>  # Get help on the command line
````
#### GLOBAL
````
git config --global user.name <username>
git config --global user.email <email>
````
#### CREATE A NEW REPOSITORY
````
git clone <repository>
cd xy
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master
````
#### EXISTING FOLDER
````
cd existing_folder
git init
git remote add origin <repository>
git add .
git commit -m "Initial commit"
git push -u origin master
````
#### EXISTING GIT REPOSITORY
````
cd existing_repo
git remote rename origin old-origin
git remote add origin <repository>
git push -u origin --all
git push -u origin --tags
````
#### CREATE
````
git clone <urltorepository>  # Clone an existing repository
git init                     # Create a new local repository
````
#### LOCAL CHANGES
````
git status         # Changed files in your working directory
git diff           # Changes to tracked files
git add .          # Add all current changes to the next commit
git add -p <file>  # Add some changes in <file> to the next commit
git commit -a      # Commit all local changes in tracked files
git commit         # Commit previously staged changes
git commit --amend # Change the last commit
````
#### COMMIT HISTORY
````
git log            # Show all commits, starting with newest
git log -p <file>  # Show changes over time for a specific file
git blame <file>   # Who changed what and when in <file>
````
#### BRANCHES & TAGS
````
git branch -av                        # List all existing branches
git checkout <branch>                 # Swicht HEAD branch
git branch <new-branch>               # Create a new branch based on your 
                                      # current HEAD
git checkout --track <remote/branch>  # Create a new tracking branch based on 
                                      # a remote branch
git branch -d <branch>                # Delete a local branch
git tag <tag-name>                    # Mark the current commit with a tag
````
#### UPDATE & PUBLISH
````
git remote -v                    # List all currently configured remotes
git remote show <remote>         # Show information about a remote
git remote add <shortname> <url> # Add new remote repository, named <remote>
git fetch <remote>               # Download all changes from <remote>, but don't 
                                 # integrate into HEAD
git pull <remote> <branch>       # Download changes and directly merge/inegrate 
                                 # into HEAD
git push <remote> <branch>       # Publich local changes on remote
git branch -dr <remote/branch>   # Delete a branch on the remote
git push --tags                  # Publish tags
````
#### MERGE & REBASE
````
git merge <branch>      # Merge <branch> into your current HEAD
git rebase <branch>     # Rebase your current HEAD onto <branch>
git rebase --abort      # Abort a rebase
git reboase --continue  # Continue a rebase after resolving conflicts
git mergetool           # Use your configured merge tool to solve conflicts
git add <resolved-file> # Use your editor to manually solve conflicts and (after 
                        # resolving) mark file as resolved
git rm <resolved-file>
````
#### UNDO
````
git reset --hard HEAD      # Discard all local changes in your working directory
git checkout HEAD <file>   # Discard local changes in a specific file
git revert <commit>        # Revert a commit (by producing a new commit with 
                           # contrary changes)
git reset --hard <commit>  # Reset your HEAD pointer to a previous commit and 
                           # discard all changes since then
git reset <commit>         # Reset your HEAD pointer to a previous commit and 
                           # preserve all changes as unstaged
git reset --keep <commit>  # Reset your HEAD pointer to a previous commit and 
                           # preserve uncommitted local changes
````
