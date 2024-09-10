### Description:
> The `git commit` command is used to save changes to your local repository. It captures the changes in your staging area (index) and adds them to the repository’s history.

**Examples**
1. Commiting the staged files with a message

    `git commit -m <"message for commit">`
   
    **Example**: `git commit -m "commit message"`
    
    **Explanation**: all the files present in the **staging area** will be committed using the message *"commit message"*.

2. Commiting the modified files directly with a message (meaning the files have not been staged but directly committed)

    `git commit -a -m <"message for commit">`
   
    **Example**: `git commit -a -m "direct commit"`
    
    **Explanation**: all the files present in the **staging area** will be committed using the message *"direct commit"*.