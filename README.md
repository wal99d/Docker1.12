# How to download and use Docker v1.12.0-rc2 on Mac OS X 
####1.First make sure you have [VirtaulBox](https://www.virtualbox.org/wiki/Downloads) installed on your machine.
####2.Download [Docker Clientv1.12-RC2](Darwin/OSX 64bit client tgz: https://test.docker.com/builds/Darwin/x86_64/docker-1.12.0-rc2.tgz) on your Mac OS X
####3.Copy the docker executable to "/usr/local/bin" as shown below:
```
cp ~/Downloads/docker/docker /usr/local/bin
```
####4.Then create a new docker machine using "docker-machine create" command as shown below, but you have to mention the new boot2docker-experimental.iso:
```
docker-machine create -d virtualbox --virtualbox-boot2docker-url https://github.com/boot2docker/boot2docker/releases/download/v1.12.0-rc2/boot2docker-experimental.iso node1
```

