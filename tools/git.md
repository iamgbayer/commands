# Git

### Disable SSL certificate checking globally 
```bash
git config --global http.sslVerify false 
```

### Users settings globally
```bash
git config --global user.name "username"
git config --global user.email "email"
```

### Undoing last commit 
```bash
git reset --soft HEAD~1
```

Also, you can create an alias to this
```bash
git config --global alias.undo "reset --soft HEAD~1"
```

### Save your credentials permanently
```
git config --global credential.helper store

```
