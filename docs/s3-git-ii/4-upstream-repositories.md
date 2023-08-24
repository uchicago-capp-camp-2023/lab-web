---
layout: default
title: Upstream Repositories
nav_order: 4
parent: Git II
---

# Working with upstream repositories

For each assignment in CAPP 30121, we provide some initial code that you must upload to your repository. We’ll use what is known as an _upstream_ repository to distribute this code.

To gain practice with this process, follow the steps below. These steps are similar to what you did at the beginning of the first Git lab with a couple of extra commands thrown in.

 1. Using a browser, accept the `git-ii` assignment invitation on canvas: https://classroom.github.com/a/JbftenWw.

 2. Navigate to your `/home/{USER}/capp30121` directory and creating a new directory named `git-ii-{GITHUB_USERNAME}` (where, as usual, `{GITHUB_USERNAME}` is replaced with your actual GitHub username).

    ```    
    cd ~/capp30121
    mkdir git-ii-{GITHUB_USERNAME}
    cd git-ii-{GITHUB_USERNAME}
    ```

 3. And then run the following commands using your GitHub username in place of `{GITHUB_USERNAME}` in the second command.

    ```        
    git init
    git remote add origin git@github.com:uchicago-capp-camp-2023/git-ii-{GITHUB_USERNAME}.git
    git remote add upstream git@github.com:uchicago-capp-camp-2023/git-ii-initial-code.git
    git pull upstream main
    git branch -M main
    git push -u origin main
    ```

    If you run an `ls`, you will see that your directory now contains two files:
    
    ```    
    hello.py  README.md
    ```
   
If you are wondering, here is what these commands do (line-by-line):

1.  `git init`: Initialize a local repository in the current working directory.
    
2.  `git remote add origin git@github.com:uchicago-capp-camp-2023/git-ii-{GITHUB_USERNAME}.git`: Connect the local repository to the repository that was created for you on GitHub when you accepted the assignment invitation.
    
3.  `git remote add upstream git@github.com:uchicago-capp-camp-2023/git-ii-initial-code.git`: Connect your local repository to an upstream GitHub repository that we have created and seeded with code for this assignment.
    
4.  `git pull upstream main`: Pull the seed code from the upstream repository into your local copy of the repository and package it into a commit. Notice that the pull command indicates that code should be pulled from the `main` branch of the _upstream_ repository.
    
5.  `git branch -M main`: Rename the branch for your local repository from `master`, a legacy name, to `main`, the preferred name.
    
6.  `git push -u origin main`: Push the current commit to GitHub. The arguments `-u origin main` tell Git that you want to push from the local copy (`origin`) to the `main` branch on GitHub. Git will remember and reuse these parameters when you run `git push` from this copy of the repository in the future.

From here on out, you can add, commit, pull, and push as usual to manage your repository. In the (hopefully) unlikely event that we need to fix a bug in the code that we provide, we’ll update the upstream repository and ask you to run `git pull upstream main`, to pull changes to the upstream code into your local copy.

{: .warning}
GIT II CHECKPOINT 2
**Before going to the next section of the lab, stop here and navigate to Gradescope to take our short quiz to review the concepts that we have covered so far in the lab.**
Link Here: https://www.gradescope.com/courses/570528/assignments

{:style="text-align:center"}
[Previous](./3-merge-conflicts.html){: .btn } [Next](./5-exercises.html){: .btn }
