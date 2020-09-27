You can now - Restream on Docker.

Install docker and connect via SSH

## Install resterm

docker pull datarhei/restreamer

docker run -d --restart always --name restreamer 
     -e "RS_USERNAME=admin" -e "RS_PASSWORD=admin" 
     -p 8080:8080 -v /mnt/restreamer/db:/restreamer/db 
     datarhei/restreamer:latest

install - rtmp restream

docker run  -p 1935:1935  datarhei/restreamer

add token to make it secure 

docker run -p 1935:1935 -e RS_TOKEN=123456 datarhei/restreamer

without token

rtmp://ip/live/external.stream

with token
rtmp://localhost/live/external.stream?token=123456
