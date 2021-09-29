# merge

Takes new commits from the branch branchname, and adds them to the current branch. If necessary, it automatically adds a "Merge" commit on top.  
`git merge branchname`  






```
git checkout -b start
git add .
git commit -m"something"
git push -u origin start
git checkout master
git merge start
git branch -d start
```

