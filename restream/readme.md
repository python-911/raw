You can now - Restream on Docker.

Install docker and connect via SSH

## Install resterm

docker run -d --restart always \
     --name restreamer \
     -e "RS_USERNAME=admin" -e "RS_PASSWORD=admin" \
     -p 8080:8080 -v /mnt/restreamer/db:/restreamer/db \
     datarhei/restreamer:latest
