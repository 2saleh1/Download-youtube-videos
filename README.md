# Download YouTube Videos with yt-dlp

A simple guide to download YouTube videos using yt-dlp with the best quality.

## 📋 Prerequisites

### 1. Update yt-dlp First!
**Always update yt-dlp before downloading to avoid errors:**
```bash
# Update yt-dlp to latest version
pip install --upgrade yt-dlp

# Or if you installed via other methods:
yt-dlp -U
```

### 2. Install Required Tools
- **yt-dlp**: `pip install yt-dlp`
- **ffmpeg**: Download from [ffmpeg.org](https://ffmpeg.org/download.html) and add to PATH

## 🚀 Simple Method (Recommended)

### Download Best Quality Video + Audio
```bash
yt-dlp -f "best[ext=mp4]" "https://www.youtube.com/watch?v=VIDEO_ID" -o "%(title)s.%(ext)s"
```

### Download Best Quality with Custom Name
```bash
yt-dlp -f "best[ext=mp4]" "https://www.youtube.com/watch?v=VIDEO_ID" -o "My_Video.mp4"
```

### Download Specific Quality (e.g., 720p)
```bash
yt-dlp -f "best[height<=720][ext=mp4]" "https://www.youtube.com/watch?v=VIDEO_ID"
```

## 🎯 Advanced Method (Manual Selection)

If you need specific formats, follow these steps:

### 1. Check Available Formats
```bash
yt-dlp -F "https://www.youtube.com/watch?v=VIDEO_ID"
```

### 2. Download with Specific Format IDs
```bash
# Example: Format 233 (audio) + Format 133 (video)
yt-dlp -f 233+133 "https://www.youtube.com/watch?v=VIDEO_ID" -o "output_name.mp4"
```

## 📁 Quick Setup

### 1. Open Command Prompt
- Press `Win + R`, type `cmd`, press Enter

### 2. Navigate to Download Folder
```bash
cd C:\Users\YourName\Downloads
# Or wherever you want to save videos
```

### 3. Run the Download Command
```bash
yt-dlp -f "best[ext=mp4]" "PASTE_VIDEO_URL_HERE"
```

## 💡 Pro Tips

### Download Entire Playlist
```bash
yt-dlp -f "best[ext=mp4]" "PLAYLIST_URL" -o "%(playlist_index)s - %(title)s.%(ext)s"
```

### Download Audio Only (MP3)
```bash
yt-dlp -x --audio-format mp3 "VIDEO_URL"
```

### Download with Subtitles
```bash
yt-dlp -f "best[ext=mp4]" --write-subs --sub-lang en "VIDEO_URL"
```

### Download from Multiple URLs
```bash
yt-dlp -f "best[ext=mp4]" -a urls.txt
```
*(Create a text file with one URL per line)*

## 🛠️ Common Issues & Solutions

### "Format not available"
```bash
# Try without format specification
yt-dlp "VIDEO_URL"

# Or use best available quality
yt-dlp -f "best" "VIDEO_URL"
```

### "ffmpeg not found"
- Download ffmpeg from official website
- Extract to a folder (e.g., `C:\ffmpeg`)
- Add `C:\ffmpeg\bin` to your system PATH

### Videos downloading as separate files
```bash
# Force merge with ffmpeg
yt-dlp -f "best[ext=mp4]" --merge-output-format mp4 "VIDEO_URL"
```

## 🎯 One-Line Solutions

### High Quality Download
```bash
yt-dlp -f "best[height<=1080][ext=mp4]" "VIDEO_URL" -o "%(title)s.%(ext)s"
```

### Quick Download (Any Quality)
```bash
yt-dlp "VIDEO_URL"
```

### Batch Download with Good Names
```bash
yt-dlp -f "best[ext=mp4]" -o "%(uploader)s - %(title)s.%(ext)s" "VIDEO_URL"
```

---

## 🚀 TL;DR - Just Want to Download?

1. **Update**: `yt-dlp -U`
2. **Navigate**: `cd C:\Users\YourName\Downloads`
3. **Download**: `yt-dlp -f "best[ext=mp4]" "PASTE_URL_HERE"`

**That's it!** ✅
