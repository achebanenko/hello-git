
Show file from repo .git/config  
`$ git config [--local] --list`

Show file ~/.gitconfig if exists  
`$ git config --global --list`


Change user's name for repo  
`$ git config [--local] user.name "yourname"`

Change users's email for repo  
`$ git config [--local] user.email "email@example.com"`


Tell Git to use the osxkeychain credentials helper  
`$ git config --global credential.helper osxkeychain`

Update credentials via MacOS Keychain Access  
If you have set credentials.helper osxkeychain on your Mac, you can update your credentials using MacOS's `Keychain Access` app.  

Deleting your credentials via the command line  
Through the command line, you can use the credential helper directly to erase the keychain entry.  
```
$ git credential-osxkeychain erase
host=github.com
protocol=https
> [Press Return]
```

