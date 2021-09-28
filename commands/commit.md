# commit

Commiting, -m allow to provide an one line message to the commit (without opening editor)
` git commit -m "Description of the commit" `


## --amend

git-scm.com/book/ru/v1/Основы-Git-Отмена-изменений  
`git commit --amend` 

Fix the identity used for the last commit (?not pushed yet)
```
git config user.name "yourname"
git config user.email "email@example.com"
git commit --amend --reset-author
```

