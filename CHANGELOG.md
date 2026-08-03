# Changelog

## v4.1
- Fixed: yt-dlp-ejs install (options 8/9) no longer fails with a PEP 668 "externally managed environment" error on macOS/Linux - dependencies now install into a dedicated virtual environment at `~/.fyresalt/venv` instead of the system Python
- Changed: Option 5 (previously the redundant "Audio only - Best format") is now an **Impersonate** submenu where you pick MP4/MKV/MP3/WAV with `--impersonate chrome` applied, for when a site is blocking or rate-limiting requests

## v4.0
- Renamed to **FYRESALT Downloader**
- New **Full Setup** option - installs all requirements in one step
- Individual tool installs moved into a dedicated **Tools** sub-menu
- macOS and Linux: dependencies now install automatically in silent mode during Full Setup

## v3.0
- Added **macOS and Linux support**
- Added **Deno JS runtime** install option - required for certain video sites
- Added **yt-dlp-ejs** install option - resolves JavaScript-related download errors
- Deno is now detected and passed automatically on every download
- Fixed: video downloads now correctly select the highest quality stream instead of a pre-muxed lower-quality file
- Fixed: long filenames (especially with non-Latin characters) no longer cause download errors
- Fixed: terminal display issues when running via one-line install command
- Added ANSI color output for a cleaner terminal experience

## v2.0
- Added color output
- Added FFmpeg install option
- Improved download progress display

## v1.0
Initial release. Windows only.
- Menu-driven interface for downloading video and audio
- Supports MP4, MKV, MP3, WAV, and playlist downloads
- Custom yt-dlp argument mode
