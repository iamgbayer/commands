# Docker


### Add the user to the docker group

Add the docker group if it doesn't already exist:

```bash
sudo groupadd docker
Add the connected user "${USER}" to the docker group:

sudo gpasswd -a ${USER} docker
Restart the Docker daemon:

sudo service docker restart
Either do a newgrp docker or log out/in to activate the changes to groups.

```


### Install composer dependencies

Runs a disposable container and install composer dependencies:

```bash
sudo docker run --rm -v $(pwd):/app composer/composer install

```
