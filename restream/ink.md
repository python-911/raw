## Hindi 

http://195.181.172.83:2200/R-EX/SPORTS_STAR_SPORTS_1_HINDI_HD-in/mono.m3u8?token=
http://185.246.210.53:2200/EX/starsports1hd-in/tracks-v1a1/mono.m3u8?token=

##English

http://89.187.169.204:2200/R-EX/SPORTS_STAR_SPORTS_1_ENGLISH_HD-in/playlist.m3u8?token=

##Restrem
english 

ffmpeg -re -i "https://prod-fastly-ap-south-1.video.pscp.tv/Transcoding/v1/hls/gMGd_SMOg32w-fuIbCx_LFO595pZEUYI_5K9peDZdq12VKDc2CcAFnjOGvr1xsAdvrVhqRcWk6wPYqs-L1Mjqw/non_transcode/ap-southeast-1/periscope-replay-direct-prod-ap-southeast-1-public/dynamic_hlsproducer.m3u8?type=live" -acodec libmp3lame -ar 44100 -b:a 128k -pix_fmt yuv420p -profile:v baseline -s 360x240 -bufsize 6000k -vb 400k -maxrate 600k -deinterlace -vcodec libx264 -preset veryfast -g 30 -r 25 -f flv "rtmp://167.71.239.179/live/low_en"

ffmpeg -re -i "http://195.181.172.83:2200/R-EX/SPORTS_STAR_SPORTS_1_HINDI_HD-in/mono.m3u8?token=" -acodec libmp3lame -ar 44100 -b:a 128k -pix_fmt yuv420p -profile:v baseline -s 420x360 -bufsize 6000k -vb 400k -maxrate 1500k -deinterlace -vcodec libx264 -preset veryfast -g 30 -r 30 -f flv "rtmp://in.pscp.tv:80/x/57e72b9zkaag"






