# Download YouTube Videos with yt-dlp

## 🔄 First: Update yt-dlp
```bash
yt-dlp -U
```

## 📋 Requirements
- **yt-dlp**: `pip install yt-dlp`
- **ffmpeg**: Download from [ffmpeg.org](https://ffmpeg.org/download.html)

## 🚀 Quick Download (Best Quality)
```bash
yt-dlp -f "best[ext=mp4]" "VIDEO_URL" -o "video_name.mp4"
```

## 🎯 Manual Format Selection

### 1. Check Available Formats
```bash
yt-dlp -F "https://www.youtube.com/watch?v=example"
```

![image](https://github.com/user-attachments/assets/389b79ce-90d3-4671-927b-723dcc563163)

### 2. Download with Specific Format IDs
```bash
# Example: Format 233 (audio) + Format 133 (video)
yt-dlp -f 233+133 "https://www.youtube.com/watch?v=VIDEO_ID" -o "output_name.mp4"
```

## 💡 Steps
1. Open Command Prompt
2. Navigate to folder: `cd C:\Users\YourName\Downloads`
3. Run the download command

**That's it!** ✅
