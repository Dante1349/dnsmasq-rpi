# docker run
```
docker run --name dnsmasq --cap-add=NET_ADMIN \
    --add-host local_url_as_desired:192.168.1.2 \
    -p "53:53/udp" milf/dnsmasq:latest
```

# docker-compose.yml
```
version: '3'

services:
  dnsmasq:
    image: milf/dnsmasq:latest
    ports:
      - "53:53/udp"
    cap_add:
      - NET_ADMIN
    extra_hosts:
      - "local_url_as_desired:192.168.1.2"
```
