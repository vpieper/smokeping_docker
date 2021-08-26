# Smokeping docker-compose with macvlan or localhost for use with reverse proxy

Smokeping docker-compose

### features

- working macvlan with docker
- latest Smokeping docker image
- systemd network devices
- each container can reach the whole nework (full routing)
- `docker-compose.yml` example with static ipv4 on macvlan
- if no ip defined, container gets an ip within `192.168.1.180/27`

### macvlan
```bash
docker network create \
                    -d macvlan \
                    -o parent=eth0 \
                    --subnet=192.168.1.0/24 \
                    --gateway=192.168.1.1 \
                    --ip-range 192.168.1.230/27 \
                    pub_net # the name
```
