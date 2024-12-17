### You want to know how many branches are currently available in your repository.

Below command will output all the *local branches*, with current branch being displayed with an `asterisk(*)` prefixing the branch name.
```cmd
git branch
```

Below command will output all the *remote branches*.
```cmd
git branch -r
```

Below command will output all the *local and remote branches*, with current branch being displayed with an `asterisk(*)` prefixing the branch name.
```cmd
git branch -a
```

### You want to know the changes you did so far comparing it with the remote branch.
- It means I have a remote branch named feature-1 in the repo and I have its local branch in my machine, so I did some changes in my local code and now I want to see what changes have I done so far.
Below command will display line by line changes for all the modified files comparing working directory and remote.
```cmd
git diff
```

Below command will display line by line changes for all the modified files comparing two branches. (consider user1 and user2 are my two branches)
```cmd
git diff user1 user2
```

Below command will display line by line changes for the file you mention. (consider main.py is the file name)
```cmd
git diff main.py
```
**NOTE**: It is necessary to type the full path of the file, that means if you are in a directory and you changed a file which is present in a folder (say `Scripts`) in your directory, so you have to type down `git diff Scripts/main.py`

### You want to send your local commits to the remote branch
- For this, you have to make sure you have saved the changes.
- Added the files into the staging area.
    - `git add .` will add all the changes to the staging area.
- Then, you've commited all the changes from the staging area with some message.
    - `git commit -m "commit message"` will commit the changes with the message specified.
- Lastly, push the commits to the remote branch.
    - `git push origin branch_name`