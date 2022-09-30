## NGNIX to RTMP

Simple docker image.

`docker run -d --name nginx-rtmp --mount type=bind,source=/HOST/htpasswd,target=/etc/nginx/htpasswd --mount type=bind,source=/HOST/nginx.conf,target=/etc/nginx/nginx.conf -p 1935:1935 -p 8080:8080 --restart=unless-stopped registry.gitlab.com/boltwolf/nginx-rtmp:latest`
