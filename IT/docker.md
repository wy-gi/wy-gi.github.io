# Docker

### 配置代理

```sh
sudo mkdir -p /etc/systemd/system/docker.service.d
sudo vim /etc/systemd/system/docker.service.d/http-proxy.conf
```

```
[Service]
Environment="HTTP_PROXY=http://192.168.124.8:10809/"
Environment="HTTPS_PROXY=http://192.168.124.8:10809/"
Environment="NO_PROXY=localhost,127.0.0.1,192.168.124.0/8,1.14.136.94"
```

```sh
sudo systemctl daemon-reload
sudo systemctl restart docker
```