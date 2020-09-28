427x240 is low streaming

## Hindi 

http://195.181.172.83:2200/R-EX/SPORTS_STAR_SPORTS_1_HINDI_HD-in/mono.m3u8?token=
http://185.246.210.53:2200/EX/starsports1hd-in/tracks-v1a1/mono.m3u8?token=

##English

http://89.187.169.204:2200/R-EX/SPORTS_STAR_SPORTS_1_ENGLISH_HD-in/playlist.m3u8?token=

##Restrem
english 

ffmpeg -re -i "http://195.181.172.83:2200/EX/beIN_Sports_13_HD-ar/tracks-v1a1/mono.m3u8?token=" -acodec libmp3lame -ar 44100 -b:a 64 -pix_fmt yuv420p -profile:v baseline -s 427x240 -bufsize 6000k -vb 400k -maxrate 600k -deinterlace -vcodec libx264 -preset veryfast -g 30 -r 25 -f flv "rtmp://puthon911.flashmediacast.com:1935/puthon911/livestream"


## 



ffmpeg -re -i "http://195.181.172.83:2200/EX/beIN_Sports_13_HD-ar/tracks-v1a1/mono.m3u8?token=" -acodec libmp3lame -ar 44100 -b:a 64k -pix_fmt yuv420p -profile:v baseline -s 426x240 -bufsize 6000k -vb 400k -maxrate 700k -deinterlace -vcodec libx264 -preset fast -g 30 -r 30 -f flv "rtmp://puthon911.flashmediacast.com:1935/puthon911"


## restream.io keys

rtmp://bangalore.restream.io/live/re_1219145_fa82dcf356d97948ac5a

primecast keys

rtmp://puthon911.flashmediacast.com:1935/puthon911







