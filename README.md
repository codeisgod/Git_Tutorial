# Github Tutorial

- Git - the most common version control system!
- Github - stores git repositories online.
- multiple online vcs are present in market like gitlab, bitbucket etc..
- A Git repo can have any type of files - code, txt, images, jar files 

## Benefits of a version control system
1. Stores history of changes made to each and every file
    1. why/what/when/who of a change
2. Makes collaboration easy

## Local and remote repository
- Repository - 
    - Folders configured to use Git
    - it has commit -> checkpoint
- Local repository - 
    - repository we have on our local system
- Remote repository - 
    - repository available online like in gitlab, github etc.

## different types of file
- two types of files in git 
    - Untracked file (U) 
    - Modified file (M)
    - Added (A) -> in staging area
- first we have to move any file/update in staging area and then commit

## Branches in Git
- Why making updates directly to the “master” branch isn’t recommended?
    - Possibility of buggy code
        - Pulled by other developers
        - Released to customers if auto-deployment is set up from master branch
- Allows to create a copy of the current master branch and work on it separately
- Avoids needing to add commits to the master branch immediately 
- Commits in the new branch can be merged to the master branch once your code is ready and tested
- Can create a branch for
    - Different features
    - Different teams
    - Different product releases (eg: Feb release)
- branch structure mostly like this
    - master -> dev -> feature_branch

## Git Commands

### git init
- To initalise git in local to any of the non git folder
```
git init
```
- `git init` will convert simple folder to reposiratory
- it will enable git inside this folder
- it will create one empty `.git` folder inside folder to make it reposiratory
- this is only first time process.

### git clone
- clone/Copy the remote repository into local
```
git clone <repo-url>
```
- for example
```
git clone https://github.com/codeisgod/Git_Tutorial.git
```
- this is only first time process.
- it will create new reposiratory in local including .git folder and also contain previous commit (if any).

### git remote add
- to link your local repository to remote
- copy local repository to remote 
```
git remote add origin <git url>
```

### git add
- Moved to staging area
    - staging area: a place throgh which we can decide what all file to be commit.
```
git add <folder or file_name>
```
- if we have to add all changes 
    - move all changes files to staging
```
git add .
```

### git commit
- commit the added file with comment message (added in local)
- before commit -> we have to use `git add`
- it creates a commit -> basically checkpoint
```
git commit -m "<Commit_message>"
```

### git push
- uploading commit to remote in the same branch where you are available
```
git push 
```
- when we are not clear with branch
```
git push <origin_name> <branch_name>
git push origin master
```

### git pull
- if sometime, remote repository is ahead of local -> to download update from remote
```
git pull origin <branch_name>
```

### git status
- to check status of git
```
git status
```

### git log
- To view all commit history
``` git log ```

### git branch
- create new branch 
```
git branch <new_branch_name>
```
- list all branch
```
git branch
```

### git checkout
- to checkout the commit -> what we did in that perticular commit -> to see codebase of any time
``` git checkout <commit_id> ```
- to comeback to latest changes
``` git checkout <master/main/branch_name> ```
- create new branch and checkout to that branch
```
git checkout -b <branch_name>
```

### git merge
- to merge from other repo to main/master repo
- be in branch where you want to branch
```
git merge <branch_to_merge>
```
- use `git push` after this to push in master

### git switch
- 
```
git switch <branch_name>
```

### git out