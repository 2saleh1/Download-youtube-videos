# Download-youtube-videos
Download youtube videos using yt-dlp 


Requirements:

You need to install "yt-dlp" and "ffmpeg"

Steps:

1. Open Command Prompt (cmd).

2. Navigate to the folder where you want to save the video by using the cd command.

Before downloading, you need to know the resolution ID for the video (MP4 only) and the audio you want to download. you can use the following command:

![image](https://github.com/user-attachments/assets/389b79ce-90d3-4671-927b-723dcc563163)

for example here I want the mp4 audio that has 233 id and the 400x244 resulotion that has 133 id 

yt-dlp -f 233 "vid url" -o "Saleh audio.mp4" && yt-dlp -f 133 "vid url" -o "Saleh vid.mp4" && ffmpeg -i "Saleh vid.mp4" -i "Saleh audio.mp4" -c:v copy -c:a aac -map 0:v -map 1:a "video_name.mp4" && del "Saleh audio.mp4" && del "Saleh vid.mp4"

Explanation:

This command will download two separate files: the audio file (Saleh_audio.mp4) and the video file (Saleh_vid.mp4).

Then, it will merge them into a single file named video_name.mp4.

Finally, it deletes the temporary audio and video files (Saleh_audio.mp4 and Saleh_vid.mp4).
