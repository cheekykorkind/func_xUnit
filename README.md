# func_xUnit
https://xunit.net/docs/getting-started/netcore/cmdline 하기가 목표

## xUnit메모
- `[Facts]` are tests which are always true. They test invariant conditions.
- `[Theories]` are tests which are only true for a particular set of data.

## memo
```
DOCKER_UID=$(id -u $USER) DOCKER_GID=$(id -g $USER) docker-compose up

docker container stop $(docker container ls -aq)
docker container rm $(docker container ls -aq)
docker rmi $(docker images -f "dangling=true" -q)
docker volume rm $(docker volume ls -qf dangling=true)
yes | docker network prune
yes | docker volume prune

docker images -a | grep "mcr.microsoft.com/dotnet/aspnet" | awk '{print $3}' | xargs docker rmi --force
```