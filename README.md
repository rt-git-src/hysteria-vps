Based on [Hysteria](https://github.com/apernet/hysteria).
## Setup VPS
### Create TLS-certificsates for your domain and starts a service to update them
`apt update && apt install -y certbot && certbot certonly --register-unsafely-without-email --standalone -d your.vps.domain⚠️ && systemctl enable certbot.timer && systemctl start certbot.timer`
### Create the server config
`mkdir -p hysteria && cd hysteria && wget https://raw.githubusercontent.com/rustamft/hysteria-vps/refs/heads/main/server.yaml?token=GHSAT0AAAAAADTSULNRQUSLBMB4WV7NRPMM2NGUS4A`
### Edit downloaded server.yaml file
### Install Docker
`curl -sSL https://get.docker.com | sh && usermod -aG docker $(whoami)`
### Run Docker container
`docker run -d -p 443:443/udp --name hysteria --restart=always -v /root/hysteria:/etc/hysteria -v /etc/letsencrypt/:/etc/letsencrypt/ --log-opt max-size=10m --log-opt max-file=5 teddysun/hysteria`
### Get and edit the [client.yaml](https://raw.githubusercontent.com/rustamft/hysteria-vps/refs/heads/main/client.yaml?token=GHSAT0AAAAAADTSULNQ2HBWHJ62AK2YM6IK2NGUYRQ)

## Setup client
- Android: [NekoBoxForAndroidPublic](https://github.com/MatsuriDayo/NekoBoxForAndroid) (for geosite routing replace "ru" with "category-ru")
- iOS: [Streisand](https://apps.apple.com/us/app/streisand/id6450534064)
