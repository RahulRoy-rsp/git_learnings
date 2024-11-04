### Description:
> The `git checkout` command is used to switch branches or restore files in your working directory. It allows you to navigate between different branches or revert changes in files to a previous state.

### Examples

1. Switch to an Existing Branch

    `git checkout <branch-name>`
   
    **Example:** `git checkout develop`
    
    **Explanation:** This command switches your working directory to the specified branch (`develop`). All your changes will reflect the state of the branch you switch to.

2. Create and Switch to a New Branch

    `git checkout -b <new-branch-name>`
   
    **Example:** `git checkout -b new_feature`
    
    **Explanation:** This command creates a new branch named `new_feature` and immediately switches to it.

3. Revert a File to the Last Committed State

    `git checkout -- <file-path>`
   
    **Example:** `git checkout -- commands/add.md`
    
    **Explanation:** This command discards changes in the specified file (`commands/add.md`) and reverts it to the state of the last commit.

4. Checkout a Specific Commit

    `git checkout <commit-hash>`
   
    **Example:** `git checkout 0fddfaf`
    
    **Explanation:** This command checks out a specific commit identified by its hash (`0fddfaf`). Your working directory will be set to the state of that commit.

5. Checkout a File from a Different Branch

    `git checkout <branch-name> -- <file-path>`
   
    **Example:** `git checkout new_feature -- commands/stash.md`
    
    **Explanation:** This command checks out a specific file (`commands/stash.md`) from a different branch (`new_feature`) without switching branches.