### Description:
> The `git merge` command is used to integrate changes from one branch into another. This command combines the histories of two branches, applying the changes from the source branch to the target branch. Merging is typically used to bring feature branches into the main branch or to integrate updates from a remote branch.

### Examples

1. Merge Another Branch into the Current Branch

    `git merge <branch-name>`
   
    **Example:** `git merge feature1`
    
    **Explanation:** This command merges the changes from the `feature1` branch into the current branch. Any new commits from `feature1` will be added to the current branch.

2. Merge with a Custom Commit Message

    `git merge <branch-name> -m "Custom merge message"`
   
    **Example:** `git merge feature1 -m "Merged from feature1 into master"`
    
    **Explanation:** This command merges the `feature1` branch into the current branch(here `master`) and provides a custom commit message for the merge commit.