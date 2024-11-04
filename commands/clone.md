### Description:
> The `git clone` command is used to create a copy of an existing Git repository. This command is typically used to obtain a repository from a remote source, such as GitHub, GitLab, or Bitbucket, and set it up on your local machine. (By default main/master branch is cloned).


**Examples**
1. Cloning a remote repository using https link
   
    `git clone <repo_url>`
   
    **Example**: `git clone https://github.com/RahulRoy-rsp/git_learnings.git`
    
    **Explanation**: it will copy the above repository (https link) into your system.

2. Cloning a remote repository using ssh link (for this you have to setup [ssh keys](https://github.com/RahulRoy-rsp/git_learnings/blob/feature1/setup_ssh_keys.txt))
   
    `git clone <repo_url>` 
   
    **Example**: `git clone git@github.com:RahulRoy-rsp/git_learnings.git`
    
    **Explanation**: it will copy the above repository (ssh link) into your system.

3. Cloning a remote repository using https link at a specified system location
   
    `git clone <repo_url> <directory-name>`
   
    **Example**: `git clone https://github.com/RahulRoy-rsp/git_learnings.git C:\Users\Desktop\repos` 
    
    **Explanation**: it will copy the above repository (https link) into your systems Desktop's repos folder.

4. Cloning a remote repository using https link for a specific branch
   
    `git clone -b <branch-name> <repo_url>`
   
    **Example**: `git clone -b feature1 https://github.com/RahulRoy-rsp/git_learnings.git`
    
    **Explanation**: it will copy the above repository's (https link) branch named *feature1* into your system.