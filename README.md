# Cheat Sheet

Hojas necesarias para la programación día a día.

# Git Cheat Sheet

## Setup


*Set a name that is identifiable for credit when review version history*
```sh
$ git config --global user.name "[firstname lastname]"
$ git config --global user.email "[valid-email]"
```

*Show global configuration* 
```sh
$ git config --get user.email
$ git config --list
```

*Open global file*
```sh
$ git config --global -e
$ git config --edit --global
```

----------
## SETUP & INIT 


*Configuring user information, initializing and cloning repositories*
```sh
$ git init
```

*Retrieve an entire repository from a hosted location via URL*
```sh
$ git clone [url]
```
----------

## STAGE & SNAPSHOT

*Show modified files in working directory, staged for your next commit*
```sh
$ git status
$ git status --short
```
*Add file as it looks now to your next commit (stage*
```sh
$ git add .
$ git add /*
$ git add *.[extension-file]
$ git add [file-name]
$ git add [/path_name]
```

*Unstage a file while retaining the changes in working directory*
```sh
$ git reset [file]
```

*time travel*
```sh
$ git reset --hard [id_commit]
$ git reset --mixed [id_commit]
$ git reset --soft [id_commit]
```


*diff of what is changed but not staged*
```sh
$ git diff
$ git diff --staged
```

*commit your staged content as a new commit snapshot | a to add*
```sh
$ git commit -m "[descriptive message]"
$ git commit -am "[descriptive message]"
```

*show the history of commit or reset*
```sh
$ git reflog
```

----------

## BRANCH & MERGE
*Isolating work in branches, changing context, and integrating changes*
```sh
$ git branch+
```

*list your branches. a * will appear next to the currently active branch*
```sh
$ git branch
```


*show or create a new branch at the current commit*
```sh
$ git branch
$ git branch [branch-name]
```

*rename branch*
```sh
$ git branch -m [old_name_branch] [new_name_branch]
```


*switch to another branch and check it out into your working directory*
```sh
$ git checkout
```

*return files to last commit *
```sh
$ git checkout -- .
```


*merge the specified branch’s history into the current one*
```sh
$ git merge [branch]
```


*show all commits in the current branch’s history*
```sh
$ git log
```

-----------
## Alias

*allows to creat shorts commands from large commands*
```sh
$ git config --global alias.[alias] "[command]"
```

*Own alias*
```sh
$ git config --global alias.s "status -sb"
$ git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
```




-----------

## Files 

**.gitignore** *file allows files to be ingonred on the stage*
```
[file].*
**/path
**/path/file
./path  
[file].[extension]
```

**.gitkeep** *allow the folder no information to be considered on the stage*
```
```

**README.md** *file containing the project description"
```
```

-----------
## GitHub

*create a new repository on the command line*
```sh
$ git init
$ git add README.md
$ git commit -m "first commit"
$ git branch -M main
$ git remote add origin https://github.com/Marduck182/Cheat-Sheet.git
$ git remote -v
$ git push -u origin main
```

*push an existing repository from the command line*
```sh
$ git remote add origin https://github.com/Marduck182/Cheat-Sheet.git
$ git branch -M main
$ git push -u origin main
```
