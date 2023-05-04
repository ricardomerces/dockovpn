# Dockovpn

Fonte: https://github.com/dockovpn/dockovpn

Server configurado com TCP

```
docker run -it --rm --cap-add=NET_ADMIN \
-p 1194:1194/tcp -p 8080:8080/tcp \
-e HOST_ADDR=$(curl -s https://api.ipify.org) \
-e HOST_TUN_PORT="443" \
--name dockovpn rmerces/openvpn
``` 