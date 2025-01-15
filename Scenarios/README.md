# Scenarios:
1. [Listing Branches](https://github.com/RahulRoy-rsp/git_learnings/tree/master/Scenarios#you-want-to-know-how-many-branches-are-currently-available-in-your-repository)
2. [Compare Changes](https://github.com/RahulRoy-rsp/git_learnings/tree/master/Scenarios#you-want-to-know-the-changes-you-did-so-far-comparing-it-with-the-remote-branch)
3. [Push local changes to remote](https://github.com/RahulRoy-rsp/git_learnings/tree/master/Scenarios#you-want-to-send-your-local-commits-to-the-remote-branch)
4. [Changes to the incorrect branch](https://github.com/RahulRoy-rsp/git_learnings/tree/master/Scenarios#you-were-doing-some-changes-in-your-local-repository-but-you-just-found-out-that-this-wasnt-the-branch-that-you-were-supposed-to-make-changes)
5. [Remote Branch not reflecting in local repository](https://github.com/RahulRoy-rsp/git_learnings/tree/master/Scenarios#you-created-a-feature-branch-in-your-github-repository-and-now-want-to-use-that-branch-in-your-code-editor-but-its-not-reflected-yet)
6. [Create branch in local repository and push it to remote](https://github.com/RahulRoy-rsp/git_learnings/tree/master/Scenarios#you-created-a-feature-branch-in-your-github-repository-and-now-want-to-use-that-branch-in-your-code-editor-but-its-not-reflected-yet)

---

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

---

### You want to know the changes you did so far, comparing it with the remote branch.
- It means I have a remote branch named *feature-1* in the repo and I have its local branch in my machine, so I did some changes in my local code and now I want to see what changes have I done so far.
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

---

### You want to send your local commits to the remote branch
- For this, you have to make sure you have saved the changes.
- Added the files into the staging area.
    - `git add .` will add all the changes to the staging area.
- Then, you've committed all the changes from the staging area with some message.
    - `git commit -m "commit message"` will commit the changes with the message specified.
- Lastly, push the commits to the remote branch.
    - `git push origin branch_name`

---

### You were doing some changes in your local repository, but you just found out that this wasn't the branch that you were supposed to make changes.

**(Scenario 1, when changes are committed)**
- You are working on a project and you created a feature branch `feature-new` from the `master` branch.
- You cloned the repo into your system and started doing changes in the code.
- Once you are satisfied with the changes, you were trying on push the changes into the remote repository.
- But then you saw that you were not making changes in the local `feature-new` branch but instead you did all the changes in the local `master` branch.
- You do not want to lose all your hardwork now or don't want to do all the changes manually again.
---
- ##### Steps to follow:
    1. Let's first stage and commit all the changes you did on your local `master` branch.
        ```cmd
        git add .
        git commit -m "Commiting all the changes"
        ```
    2. Switch to the local feature branch `feature-new`.
        ```
        git checkout feature-new
        ``` 
    3. Copy the commit hash from the local master branch
        ```
        git log master
        ```
    4. Once copied the hash of the commit, apply that commit to the feature branch
        ```
        git cherry-pick <hash>
        ```
    5. See if all the changes are applied to the feature branch
    6. Push the changes to remote branch
        ```
        git push origin feature-new
        ```
    7. Now, let's make the local master branch same as remote master.
        ```
        git checkout master
        git reset --hard origin/master
        ```
---
**(Scenario 2, when changes are not committed)**
- You are working on a project and you created a feature branch `feature-new` from the `master` branch.
- You cloned the repo into your system and started doing changes in the code.
- Once you are satisfied with the changes, you were trying to commit the changes.
- But then you saw that you were not making changes in the local `feature-new` branch but instead you did all the changes in the local `master` branch.
- You do not want to lose all your hardwork now or don't want to do all the changes manually again.
---
- ##### Steps to follow:
    1. Make sure all the changes are being staged.
        ```cmd
        git add .
        ```
    2. Stash your changes (make sure you are in local `master` branch).
        ```cmd
        git stash save "stash-from-master"
        ```
    3. Switch to the local `feature-new` branch
        ```cmd
        git checkout feature-new
        ```
    4. (Optional Step) view the list of stash available. `git stash list`
    5. From the list you can see that its the most recent stash that you want to use in your feature branch.
    6. Apply the changes to the feature branch.
        ```cmd
        git stash apply stash@{0}    
        ```
        - You could also do `git stash apply` this will apply the most recent stash to the branch.
        - You could have also done `git stash pop` this will also apply the most recent stash to the branch, and it will remove the entry from the stash.
    7. Once, the stash has been applied you can stage, commit and push the changes and also clean the stash.

---

### You created a feature-branch in your Github repository and now want to use that branch in your Code editor, but its not reflected yet

- Let's say you created a branch in a repository in Github. (suppose branch name is `branch-android`)
- Now you visit your Code editor and tried to switch to this branch.
- But unfortunately, you couldn't because it says `this branch is not available`.
- So, you listed all the branches and yes, you see that this newly created branch branch is not reflected in your local git repository.
---
##### Steps to resolve
- Bring all the updates from the remote repository.
    ```bash
    git fetch origin
    ```
- Now switch to the branch
    ```bash
    git checkout branch-android
    ```

---

### You want to create a feature branch in local from a branch in cloud and do the changes and push it to the cloud.

- Let's take an example, you are a developer and you have been assigned a task.
- Now, first thing as a good developer you do not make changes directly to the master branch but to create a branch from the master branch and do the changes in there and then push the changes to the master branch.
---
- ##### Steps to follow:
    - Make sure that you are in the `master branch` in your code editor.
    ```bash
    git checkout master
    ``` 
    - Bring all the changes from the remote master branch to the local master branch. (this makes sure that we are having the up-to-date repo)
    ```bash
    git pull origin
    ```
    - Now, lets create a `feature-branch` from the `master branch`.
    - Let's say we want to name our branch as `feature-for-upgrade`
        ```bash
        git checkout -b feature-for-upgrade
        ```
    - Do the changes and push the branch to the remote repository.
        ```bash
        git push origin feature-for-upgrade
        ```

---
