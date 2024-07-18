# Branching, Merging, and Rebasing in Git

This document explains essential Git concepts for managing code changes: branching, merging, and rebasing. It includes clear commands for common scenarios and helps you decide when to use each approach.

## Understanding Branching:

    A branch is a separate line of development in your Git repository.
    It allows you to work on changes without affecting the main codebase (master branch by default).

* Merging vs. Rebasing:

    Merging: Creates a new commit that combines changes from two branches, preserving their history.
    Rebasing: Rewrites commit history by applying one branch's changes (e.g., Greet) on top of another's (e.g., main).

* Choosing Between Merging and Rebasing:
    Merging: Preferred for: 
    
      Collaboration: Clear history of how branches evolved.
      Independent work: Preserves individual changes.
        
       
    Rebasing:      
        Maintaining a clean local history (before pushing).
        Linear history (consider private repositories).

Caution with Rebasing:
`N/B`
    Rewrites history, potentially causing issues on shared repositories (remote conflicts).
    Use with caution in public repositories to avoid confusing history for others.

## Common Scenarios and Commands:

1. Merging Main into Greet Branch (Conflict):

a. Switch to Greet branch:

  ```bash
  git checkout Greet
  ```

b. Attempt merge:

  ```bash
  git merge main
  ```
2. Resolving Conflicts:

a. Open hello.sh in a text editor.
b. Manually edit the file:
check on incomming changes
- Keep desired changes from each branch.
c. Stage the resolved file:

  ```bash
  git add hello.sh
  ```

d. Commit the merge:

  ```bash
  git commit -m "Resolved conflicts in hello.sh"
  ```

3. Rebasing Greet Branch:

    Rebasing rewrites history by integrating changes from one branch (Greet) onto another (main).

Note: While this creates a cleaner local history, use caution in public repositories.

a. Switch to Greet branch:

  ```bash
  git checkout Greet
  ```

b. Rebase onto main:

  ```bash
  git rebase main
  ```

  -`N/B` This rewrites history. Conflicts might arise during rebasing. Resolve them as explained in step 2.

4. Merging Greet into Main:

 first Switch to main branch: and then carry out the merging process.
  
``` bash
    git checkout main
```

Merge Greet:
``` bash
git merge Greet
 ```



