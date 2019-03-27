
## Config

1. Create trojan config `/etc/trojan/config.json`.

2. Modify local address to "0.0.0.0".

```json
    "local_addr": "0.0.0.0"
```

2. Move cert and key to `/etc/trojan/`.

```json
    "cert": "/etc/trojan/fullchain.pem",
    "key": "/etc/trojan/privkey.pem"
```

## Pull

```bash
$ docker pull bubbling/trojan-docker
```

## Run
```bash
$ docker run -d --name=trojan --restart always -p 443:443 -v /etc/trojan:/etc/trojan bubbling/trojan-docker
```
