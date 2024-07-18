# Conflicts, merging and rebasing

## Merge Main into Greet Branch
a. Switch to Greet Branch:

```Bash
git checkout Greet

```
b. Pull Latest Changes :

``` bash
git pull origin main
```
c. and lastly merge main into Greet

``` bash
git merge main
```

## Switch to main branch and make changes to hello.sh file
 a. Switch to Greet branch:

  ```bash
  git checkout main
 ```
 b. switch to the lib/ directory and make changes in hello.sh
    `N/B` you are in the parent directory :
  ```bash
  cd work/hello/lib/
 ```
 `N/B` if all the changes in this branch are not yet committed then commit and push the changes. you can even temporarily save your work when moving to another branch 
   ```bash
 git stash
 ```
 and then stash them back when you get back to this branch
   ```bash
git stash apply
 ```
## Merging Main into Greet Branch (Conflict)
a. Switch to Greet branch:

  ```bash
  git checkout Greet
  ```

b. Attempt merge:

  ```bash
  git merge main
  ```

## Resolve the conflict (manually or using merge tools)
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

## After resolving, stage the changes and commit

c. Stage the resolved file:

  ```bash
  git add hello.sh
  ```

d. Commit the merge:

  ```bash
  git commit -m "Resolved conflicts in hello.sh"
  ```


## Rebasing Greet Branch
a. Switch to Greet branch:

  ```bash
  git checkout Greet
  ```

b. Rebase onto main:

  ```bash
  git rebase main
  ```


## Merging Greet into Main

 first Switch to main branch: and then carry out the merging process.
  
``` bash
    git checkout main
```

Merge Greet:
``` bash
git merge Greet
 ```


