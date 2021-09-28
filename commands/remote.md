# Remote

username - your username  
repo - name of your repo  

Add remote  
` git remote add origin https://github.com/username/repo.git `

To store your personal access token  
` git remote add origin https://username:access-token@github.com/username/repo.git `

Shows the remote's shortname  
`git remote`

Shows the URLs that Git has stored for the shortname to be used when reading and writing to that remote  
`git remote -v`

Info on both 'pull' and 'push' configuration per branch  
`git remote show origin`

Deletes remote github
`git remote remove github`  


## set-url

https://help.github.com/en/articles/changing-a-remotes-url  
` git remote set-url origin https://github.com/username/repo.git `

A common mistake is cloning using the default (HTTPS) instead of SSH - update url to correct this  
` git remote set-url origin git@github.com:username/repo.git `

Avoid username password when `git push` - ?maybe not the best way  
` git remote set-url origin https://username:password@github.com/repo.git `

