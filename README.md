## Setup VPS
`docker run -d -p 443:443/udp --name hysteria --restart=always -v /root/hysteria:/etc/hysteria -v /etc/letsencrypt/:/etc/letsencrypt/ teddysun/hysteria`

## Setup client
- Android: [NekoBoxForAndroidPublic](https://github.com/MatsuriDayo/NekoBoxForAndroid) (for geosite routing replace "ru" with "category-ru")
