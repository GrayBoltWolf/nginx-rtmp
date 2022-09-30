## NGNIX to RTMP

Simple docker image.

`docker run -d --mount type=bind,source=/HOST/htpasswd,target=/etc/nginx/htpasswd --mount type=bind,source=/HOST/nginx.conf,target=/etc/nginx/nginx.conf -p 1935:1935 -p 8086:8080 registry.gitlab.com/boltwolf/nginx-rtmp:latest`
