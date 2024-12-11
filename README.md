# Download-youtube-videos
Download youtube videos using yt-dlp 


------------ You need to install "yt-dlp" and "ffmpeg"  ---------------

1: Open cmd 

2: navigate to the folder that you want to save the video on by using : cd command

at first you need to know the resolution id for your video and audio that you want to download, simply you need to write :

yt-dlp -F "https://www.youtube.com/watch......."

![image](https://github.com/user-attachments/assets/389b79ce-90d3-4671-927b-723dcc563163)

for example here I want the mp4 audio that has 233 id and the 400x244 resulotion that has 133 id 

yt-dlp -f 233 "vid url" -o "Saleh audio.mp4" && yt-dlp -f 133 "vid url" -o "Saleh vid.mp4" && ffmpeg -i "Saleh vid.mp4" -i "Saleh audio.mp4" -c:v copy -c:a aac -map 0:v -map 1:a "video_name.mp4" && del "Saleh audio.mp4" && del "Saleh vid.mp4"

