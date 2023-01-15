## NGNIX to RTMP

Simple docker image to stream RTMP video with some form of access control.

`docker run -d --name nginx-rtmp --mount type=bind,source=/HOST/htpasswd,target=/etc/nginx/htpasswd --mount type=bind,source=/HOST/nginx.conf,target=/etc/nginx/nginx.conf -p 1935:1935 -p 8080:8080 --restart=unless-stopped docker pull ghcr.io/grayboltwolf/nginx-rtmp:latest`

RTMP server: `rtmp://SERVER_IP/live`

Stream key: `YOUR_NAME?psk=ACCESSKEY`

Access key in the stream key is what you configure in the nginx.conf.

View in VLC: `rtmp://SERVER_IP/live/YOUR_NAME`
