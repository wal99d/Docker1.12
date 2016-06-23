# How-to Docker v1.12.0-rc2 on Mac OS X 
##  Download and Use 
* First make sure you have [VirtaulBox](https://www.virtualbox.org/wiki/Downloads) installed on your machine.
* Download [Docker Clientv1.12-RC2](Darwin/OSX 64bit client tgz: https://test.docker.com/builds/Darwin/x86_64/docker-1.12.0-rc2.tgz) on your Mac OS X
* Copy the docker executable to "/usr/local/bin" as shown below:
```
cp ~/Downloads/docker/docker /usr/local/bin
```
* Then create a new docker machine using "docker-machine create" command as shown below, but you have to mention the new boot2docker-experimental.iso:
```
docker-machine create -d virtualbox --virtualbox-boot2docker-url https://github.com/boot2docker/boot2docker/releases/download/v1.12.0-rc2/boot2docker-experimental.iso node1
```

## Creating a SWARM and adding/listing nodes
* On the manager node issue the below command to init the swarm:
```
#docker swarm init
```

* On other machines issue below command to join the swarm by porviding the manager node's name and port as below:
```
#docekr swarm join MANAGER_NODE:PORT 
```

* Repeat the above step to add other nodes to the swarm

**Listing Nodes in swram:**
use this command: 
```
#docker node ls
``` 





