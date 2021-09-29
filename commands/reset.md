# reset

git-scm.com/book/ru/v2/Инструменты-Git-Раскрытие-тайн-reset  
`git reset` 

Moves HEAD to commit  
`git reset --hard <commit-hash>` 


Squash the last 3 commits  
```
git reset --soft HEAD~3 &&
git commit -m"New commit"
```

