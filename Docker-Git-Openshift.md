# Docker

## JBoss

```
#Get more JBoss logs:
journalctl -f
```

## Git

```
#Create tag:
git pull
git tag 1.2.1
git push origin 1.2.1

# User name + email config
git config user.name "Name"
git config --global user.email "Email"
```

## Docker

```
#Build and publish an image manually:
docker build -t someName:0.1 .
docker tag -f someName:0.1 dockerhub.someUrl/someName:0.1
docker push someUrl/someName:0.1
```

Aliases in `~/.bashrc`:
```
alias dk='CONTAINER=$(docker ps -q) && docker kill $CONTAINER && docker rm $CONTAINER'
alias drm='docker rm -f  $(docker ps -q)'
alias dps='docker ps'

de () { docker exec -it "$@" bash; }

#dl () { docker logs -f "$@"; }
# not using docker logs as limited output is not possible : here 1000 lines
dl () { sudo tail -1000f `docker inspect -f '{{ .LogPath }}' "$@"`; }
```

Docker conf:
```
sudo groupadd docker
sudo gpasswd -a ${USER} docker

sudo vi /etc/sysconfig/docker
ADD_REGISTRY='--add-registry someUrl --add-registry registry.access.redhat.com'
INSECURE_REGISTRY='--insecure-registry someUrl'

sudo systemctl stop docker
sudo systemctl start docker
```
