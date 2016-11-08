# Git

### Disable SSL certificate checking globally 
```bash
git config --global http.sslVerify false 
```

### Clean containers with status exited
```bash
docker rm -f $(docker ps -f status=exited -q | tr '\r\n' ' ')
```
