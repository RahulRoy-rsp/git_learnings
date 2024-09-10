### Description:
> The `git stash` command is used to temporarily save changes in your working directory that are not yet ready to be committed. This allows you to switch branches or perform other tasks without committing incomplete work. The stashed changes can later be reapplied to your working directory.

### Examples

1. Stash Uncommitted Changes

    `git stash`
   
    **Example:** `git stash`
    
    **Explanation:** This command saves your uncommitted changes and reverts your working directory to match the HEAD commit. The changes are stored in a new stash entry.

2. Stash Changes with a Message

    `git stash push -m "custom message"`
   
    **Example:** `git stash push -m "stashed because switching to new branch"`
    
    **Explanation:** This command saves your uncommitted changes with a custom message. This helps to identify the stash later.

3. List All Stashed Changes

    `git stash list`
   
    **Example:** `git stash list`
    
    **Explanation:** This command lists all the stash entries.

4. Apply the Most Recent Stash

    `git stash apply`
   
    **Example:** `git stash apply`
    
    **Explanation:** This command re-applies the most recent stash entry to your working directory without removing it from the stash list.

5. Apply a Specific Stash

    `git stash apply stash@{<index>}`
   
    **Example:** `git stash apply stash@{1}`
    
    **Explanation:** This command re-applies a specific stash entry identified by its index (here the index is 1). Replace `<index>` with the appropriate number from `git stash list`.

6. Drop a Specific Stash

    `git stash drop stash@{<index>}`
   
    **Example:** `git stash drop stash@{1}`
    
    **Explanation:** This command removes a stash entry at index 1 from the list. Replace `<index>` with the appropriate number from `git stash list`.

7. Clear All Stashes

    `git stash clear`
   
    **Example:** `git stash clear`
    
    **Explanation:** This command removes all stash entries, clearing the stash list entirely.