## You can now - Restream on Docker.

## finally change video quality to. 384x160. - 480x200

Install docker and connect via SSH

## Install resterm

low live.json file - 

goto /var/lib/docker/overlay2

find -name live.json 
edit live.json and add

"-s 427x240",



#install official

docker pull datarhei/restreamer

docker run -d --restart always \
     --name ss1 \
     -e "RS_USERNAME=admin" -e "RS_PASSWORD=admin" \
     -p 8080:8080 -v /mnt/ss1/db:/restreamer/db \
     datarhei/restreamer:latest

## install - rtmp restream

docker run  -p 1935:1935  datarhei/restreamer

## add token to make it secure 

docker run -p 1935:1935 -e RS_TOKEN=123456 datarhei/restreamer

## Own server will stream now.

rtmp://ip/live/external.stream
with token
rtmp://ip/live/external.stream?token=123456

# watch live stream from own server
rtmp://ip/live/external.stream

-_-_-_-_-_-_
ADD ANOTHER 3 containers - 
default container is for low_en

# enhd - English HD Stream hd_en
docker run -d --restart always \
     --name ss2 \
     -e "RS_USERNAME=admin" -e "RS_PASSWORD=admin" \
     -p 8082:8080 -v /mnt/ss2/db:/restreamer/db \
     datarhei/restreamer:latest

# enhd - Hindi HD Stream hd_hi
docker run -d --restart always \
     --name ss3 \
     -e "RS_USERNAME=admin" -e "RS_PASSWORD=admin" \
     -p 8084:8080 -v /mnt/ss3/db:/restreamer/db \
     datarhei/restreamer:latest
# enhd - English Low Stream low_hi
docker run -d --restart always \
     --name ss4 \
     -e "RS_USERNAME=admin" -e "RS_PASSWORD=admin" \
     -p 8086:8080 -v /mnt/ss4/db:/restreamer/db \
     datarhei/restreamer:latest

## now four servers.

http://167.71.239.179:8080/ : 
rtmp://167.71.239.179/live/low_en

http://167.71.239.179:8082/
rtmp://167.71.239.179/live/hd_en

http://167.71.239.179:8084/
rtmp://167.71.239.179/live/low_hi

http://167.71.239.179:8086/
rtmp://167.71.239.179/live/hd_hi
