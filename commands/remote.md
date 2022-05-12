# Remote

username - your username  
repo - name of your repo  

### Add remote  

`$ git remote add origin https://github.com/username/repo.git`

Store your personal access token  
`$ git remote add origin https://username:access-token@github.com/username/repo.git`

### Remote info

Shows the remote's shortname  
`$ git remote`

Shows the URLs that Git has stored for the shortname to be used when reading and writing to that remote  
`$ git remote -v`

Info on both 'pull' and 'push' configuration per branch  
`$ git remote show origin`

### set-url

Changing a remotes url  
`$ git remote set-url origin https://github.com/username/repo.git`

Update url to use SSH  
` git remote set-url origin git@github.com:username/repo.git `

Avoid username and password when `$ git push` (?maybe not the best way)  
`$ git remote set-url origin https://username:password@github.com/repo.git `


### Rename

Change remote name from 'origin' to 'destination'  
`$ git remote rename origin destination`  

### Remove

Removing the remote URL from your repository only unlinks the local and remote repositories. It does not delete the remote repository.  

`$ git remote remove <reponame>`  
?OR `$ git remote rm <reponame>`  


