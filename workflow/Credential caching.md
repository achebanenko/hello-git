# ??old Enable credential caching

https://stackoverflow.com/questions/6565357/git-push-requires-username-and-password  

```
$ git config credential.helper store
$ git push https://github.com/owner/repo.git
> Username for 'https://github.com':
> Password for 'https://USERNAME@github.com':
```

You should also specify caching expire, after enabling credential caching, it will be cached for 7200 seconds (2 hour)  
`$ git config --global credential.helper 'cache --timeout 7200'`  
