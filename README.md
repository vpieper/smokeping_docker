# smokeping
Smokeping docker-compose
Create Docker macvlan network with:

```docker network create -d macvlan --subnet=192.168.2.0/16 --gateway=192.168.1.1  -o parent=eth0 pub_net```
