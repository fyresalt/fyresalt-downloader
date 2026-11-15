# Changelog

## v4.1
- Fixed: yt-dlp-ejs install (Full Setup / Tools) no longer fails with a PEP 668 "externally managed environment" error on macOS/Linux - dependencies now install into a dedicated virtual environment at `~/.fyresalt/venv` instead of the system Python
- Changed: Option 5 (previously the redundant "Audio only - Best format") is now an **Impersonate** submenu where you pick a video or audio format with `--impersonate chrome` applied, for when a site is blocking or rate-limiting requests
- Fixed: the JS runtime step no longer treats node/bun as sufficient. Deno is required for yt-dlp-ejs, so it is now installed when missing (previously Full Setup skipped it, then yt-dlp-ejs failed with "Deno is not installed"). Error messages now point to the Tools menu instead of the removed option 11
- Added: **MP4 HD** option (also in the Impersonate menu and the GUI) - picks the highest resolution first, then prefers MP4/M4A. Option 1 can cap at 1080p when higher resolutions are only offered as VP9/WebM
- Changed: the main menu is smaller. Formats moved into a **Video** page (MP4, MKV, MP4 HD) and an **Audio** page (MP3, WAV). Menu numbers changed: Playlist is 3, Custom 4, Impersonate 5, Full Setup 6, Tools 7
- Added: **Original** audio option (best available audio, no conversion) on the Audio and Impersonate pages
- Fixed: on macOS the yt-dlp-ejs plugin was copied to a folder yt-dlp does not read, so it never loaded. It now goes to `~/.config/yt-dlp/plugins` (or `$XDG_CONFIG_HOME`), same as Linux
- Fixed: on Linux the standalone yt-dlp binary is now downloaded (x86_64 and aarch64) instead of the Python zip build, so the Impersonate options work
- GUI: window is taller so the output log is not squeezed by the new options
- Fixed: on macOS/Linux the launcher quit right after showing its first menu when run as `curl ... | bash` or `| sh`; it now waits for your answer
- Fixed: Macs with no Python and no Homebrew can now get set up. The launcher offers Apple's Command Line Tools (includes Python 3), and Full Setup installs Deno with the official installer and offers to install Homebrew for FFmpeg
- Changed: yt-dlp-ejs is skipped with a clear message on Python older than 3.10 (Apple's Command Line Tools Python is 3.9) instead of failing with "pip install failed"

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
