# FYRESALT Downloader

A cross-platform terminal downloader for videos and other sites, A frontend for yt-dlp.

## Quick Start

**Windows** - open PowerShell or Windows Terminal and run:
```powershell
irm get.fyresalt.com | iex
```

**macOS / Linux** - open Terminal and run:
```bash
curl -fsSL get.fyresalt.com/mac | bash
```

The script runs entirely from memory and downloads files to your Videos folder (or Movies on macOS).

---

## Menu Options

| Option | Description |
|--------|-------------|
| 1 | Download video + audio as MP4 (best quality) |
| 2 | Download video + audio as MKV (best quality) |
| 3 | Download audio only as MP3 (high quality) |
| 4 | Download audio only as WAV (high quality) |
| 5 | Download audio only (best available format) |
| 6 | Download playlist - organizes each playlist into its own folder |
| 7 | Custom yt-dlp arguments |
| 8 | Install/Update all requirements at once |
| 9 | Install/Update required tools individually |
| 0 | Exit |

---

## Requirements

### Windows
- Windows Terminal https://aka.ms/terminal (Optional)
- PowerShell 5.1+ (Built into Windows 10/11)
- yt-dlp - install via option 8
- FFmpeg - install via option 8
- Deno - install via option 8 (Needed for YouTube EJS support)

### macOS
- Python 3 (pre-installed on macOS)
- yt-dlp - install via option 8
- FFmpeg - install via option 8 (brew install ffmpeg)
- Deno - install via option 8 (brew install deno)

### Linux
- Python 3 (Pre-installed on most distros)
- yt-dlp - install via option 8
- FFmpeg - install via your package manager (Prompted in option 8)
- Deno - install via option 8

---

## YouTube EJS Fix

Newer versions of yt-dlp require a JavaScript runtime to extract some YouTube formats. If you see the warning:

    No supported JavaScript runtime could be found.

Run option 9 first (Install/Update all requirements at once)
