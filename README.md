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
| 1 | Video page - MP4 (most compatible), MKV (best quality), MP4 HD (max resolution, may use VP9/AV1 so less compatible) |
| 2 | Audio page - MP3 (high quality), WAV (high quality), Original (best available audio, no conversion) |
| 3 | Download playlist - organizes each playlist into its own folder |
| 4 | Custom yt-dlp arguments |
| 5 | Impersonate - same formats with browser impersonation (bypass blocks) |
| 6 | Install/Update all requirements at once |
| 7 | Install/Update required tools individually |
| 0 | Exit |

---

## Requirements

### Windows
- Windows Terminal https://aka.ms/terminal (Optional)
- PowerShell 5.1+ (Built into Windows 10/11)
- yt-dlp - install via option 6
- FFmpeg - install via option 6
- Deno - install via option 6 (Needed for YouTube EJS support)

### macOS
- Python 3 (pre-installed on macOS)
- yt-dlp - install via option 6
- FFmpeg - install via option 6 (brew install ffmpeg)
- Deno - install via option 6 (brew install deno)

### Linux
- Python 3 (Pre-installed on most distros)
- yt-dlp - install via option 6
- FFmpeg - install via your package manager (Prompted in option 6)
- Deno - install via option 6

---

## YouTube EJS Fix

Newer versions of yt-dlp require a JavaScript runtime to extract some YouTube formats. If you see the warning:

    No supported JavaScript runtime could be found.

Run option 6 first (Install/Update all requirements at once)
