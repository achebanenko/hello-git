Ref:  
https://git-scm.com/book/it/v2/Git-Basics-Working-with-Remotes  
https://git-scm.com/docs

---

`git init` # initialising  
`touch .gitignore` # create new file .gitignore

`git add file1.txt` # this command actually signaling (not send) that we want this file to participate in the next commit  
`git add .` OR `git add -A` # adding all files

`git commit -m"first commit"` # commiting, -m allow us to provide a message to the commit  
`git commit --amend` # git-scm.com/book/ru/v1/Основы-Git-Отмена-изменений

`git status`  
`git diff`  
`git log`  
`git reflog` # show last commits and hashes

`git reset` # git-scm.com/book/ru/v2/Инструменты-Git-Раскрытие-тайн-reset

`rm .DS_Store` # remove something

`git remote add origin https://github.com/art-optimise/pokedex-redux.git`  
`git push -u origin master`

`git remote set-url origin https://github.com/artchebanenko/kode-intern-test.git` # https://help.github.com/en/articles/changing-a-remotes-url  
If you're updating to use SSH, your URL might look like: git@github.com:USERNAME/REPOSITORY.git  
`git remote set-url origin https://name:password@github.com/repo.git` # avoid username password when `git push` - ?maybe not the best way  
`git remote set-url origin git@github.com:username/repo.git` # a common mistake is cloning using the default (HTTPS) instead of SSH - update url to correct this

`git branch` `git branch -a` `git branch -v` `git branch -av` # This will list all branches that exist  
`git branch -vv` # gives you all tracking branches (configured for 'pull')

`git checkout master`  
`git checkout -b start` # switched to a new branch 'start' (checkout a new branch)  
`git push -u origin start` # branch start set up to track remote branch start from origin.

`git remote` # shows the remote's shortname  
`git remote -v` # shows you the URLs that Git has stored for the shortname to be used when reading and writing to that remote  
`git remote show origin` # info on both 'pull' and 'push' configuration per branch

`git remote remove github` # deletes remote github

`git reset --hard <commit-hash>` # moves HEAD to commit

With an escape hatch --allow-unrelated-histories option to be used in a rare event that merges histories of two projects that started their lives independently.
