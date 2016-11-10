# Docker


### Add the user to the docker group

Add the docker group if it doesn't already exist:
```bash
sudo groupadd docker
```

Add the connected user "${USER}" to the docker group:
```bash
sudo gpasswd -a ${USER} docker
```

Restart the Docker daemon:
```bash
sudo service docker restart
```

### Run command in disposable container

Runs a disposable container and also execute a command in with specific image:

```bash
sudo docker run --rm -v $(pwd):/app composer/composer install
```

### Delete containers with status exited
```bash
docker rm -f $(docker ps -f status=exited -q | tr '\r\n' ' ')
```
