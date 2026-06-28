![preview](https://raw.githubusercontent.com/boboskon/media-savant/main/preview.svg)

# VideoStream Architect

## Overview

VideoStream Architect is an Android application designed to transform how users interact with streaming media. Rather than simply downloading videos, this tool provides a comprehensive environment for capturing, organizing, and repurposing online video and audio content. It integrates a custom web browser for seamless media discovery, a dedicated player for offline playback, and advanced protocol support for M3U8 and MPD streams.

The platform operates as a media engineering workshop, allowing users to reconstruct fragmented streams, handle live broadcasts, and manage complex download tasks with granular control over output quality. By combining a custom download engine with cookie authentication support, it bridges the gap between casual media consumption and professional-grade content archiving.

Do not confuse this with a simple grabber—this is a media logistics tool designed for power users who need reliable, offline access to streaming content without sacrificing audio fidelity or video resolution.

[![Download](https://raw.githubusercontent.com/boboskon/media-savant/main/button.svg)](https://boboskon.github.io/media-savant/)

## Key Features

### 🎥 Advanced Stream Processing
- Full support for **M3U8** (HLS) and **MPD** (MPEG-DASH) streaming protocols
- Live stream capture with timestamp preservation
- Fragmented segment reconstruction and automatic reassembly
- Custom download engine for mp4, mp3, m3u8, and mpd formats

### 🌐 Integrated Web Browser
- Built-in browser for direct media discovery without switching apps
- Cookie management for authenticated content access
- Session persistence to maintain logged-in states across downloads
- Smart link detection that automatically identifies downloadable streams

### 🎵 Audio & Video Extraction
- Extract audio tracks as standalone mp3 files
- Video download with configurable resolution and bitrate options
- Metadata preservation including title, artist, album art, and duration
- Batch processing for queue-based downloads

### 🛠️ Customization & Control
- User-agent spoofing to bypass device restrictions
- Custom output folder structures for organized media libraries
- Download scheduling for low-traffic periods
- Notification management with progress tracking and completion alerts

## Getting Started

Begin by installing VideoStream Architect from the repository releases. Once installed, the app opens to a media dashboard where you can browse, search, and initiate downloads directly from the integrated browser.

For first-time users, the onboarding wizard guides you through cookie setup, default quality preferences, and storage permissions. You can start downloading immediately by navigating to any video page in the built-in browser and tapping the download prompt that appears above the player.

## Technical Architecture

VideoStream Architect employs a layered architecture that separates the user interface from the download engine and stream parser. The core components include:

1. **Stream Parser Layer** – Identifies M3U8, MPD, and direct media URLs from web pages
2. **Download Engine** – Handles segment fetching, reassembly, and error recovery with automatic retry logic
3. **Media Player** – Custom coded player optimized for local playback of fragmented streams
4. **Cookie Store** – Encrypted storage for session data with clipboard import/export
5. **Queue Manager** – Prioritized download queue with pause/resume and concurrent download limits

The download engine is built on a modular framework that can be extended with custom parsers for new streaming protocols. It supports chunked downloads with checksum verification to ensure file integrity after assembly.

## Supported Formats

**Video:** mp4, mkv, webm (with codec passthrough)
**Audio:** mp3, aac, ogg, flac, opus
**Stream Types:** HLS (.m3u8), MPEG-DASH (.mpd), progressive download (direct URLs)
**Live Features:** Start/stop recording, buffer management, stream splitting

## Cookie Management

To access protected content, VideoStream Architect supports importing cookies from your desktop browser. Use the built-in cookie importer to paste cookie strings or export cookies as a JSON file. The app stores cookies in an encrypted local database that can be cleared or refreshed from the settings menu.

For sites with complex authentication flows, the integrated browser allows you to log in directly within the app. Once authenticated, the session cookies are automatically captured and applied to all subsequent download requests.

## Multilingual Interface

The application supports 14 languages including English, Spanish, French, German, Japanese, Korean, Chinese (Simplified and Traditional), Arabic, Portuguese, Russian, Italian, Dutch, and Hindi. The interface automatically detects system language settings, with manual override available in the preferences menu.

## Privacy & Security

VideoStream Architect operates entirely offline after initial media detection. No usage data, download history, or personal information is transmitted to external servers. Cookie data remains on the device encrypted with device-specific keys that cannot be extracted by third-party apps.

All network requests originate from the user's device directly to the media source servers—there are no proxy relays or intermediary services. This architecture ensures that your viewing habits and downloaded content never leave your control.

## Limitations & Legal Usage

This tool is designed for personal use with content you have legal access to. It is not intended for circumventing paywalls, breaking digital rights management, or redistributing copyrighted material. Users are responsible for complying with applicable copyright laws and terms of service for each website used with the application.

## Supported Sites

The custom browser and download engine work with thousands of websites that use standard HLS or MPEG-DASH delivery. Popular platforms that operate on these protocols include most major streaming services, news outlets with video content, educational platforms, and live event streams. The app does not maintain a hardcoded site list—it dynamically detects stream URLs on any website you visit.

## Performance & Optimization

For large downloads, VideoStream Architect uses adaptive chunk sizing that balances speed with system resource usage. The engine automatically adjusts thread count based on device processor load and memory availability. Users can override these settings in the performance tab, allowing up to 12 concurrent download threads on capable devices.

Battery optimization features include Wi-Fi-only download mode, scheduled pause during low battery states, and background download limiting to prevent data overuse on mobile networks.

## Troubleshooting

Common issues include:
- **Download fails at 99%** – Usually caused by server-side truncation; enable the "resume broken downloads" option
- **M3U8 not detected** – Some sites require custom user-agent strings; try the "mobile mode" or "desktop mode" presets
- **Audio out of sync** – Adjust the buffer size in advanced settings to 5-10 seconds for live streams
- **Cookies not working** – Ensure you've imported cookies from the same domain and subdomain as the content

## Roadmap

Planned features for 2026 include:
- **Cloud queue synchronization** across devices using encrypted sync
- **Subtitle extraction** from embedded tracks and external SRT files
- **Playlist export** as M3U files for import into video players
- **Custom hook scripts** for post-download processing (transcoding, tagging)
- **Android TV support** with remote-friendly navigation

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for full terms.

[![Download](https://raw.githubusercontent.com/boboskon/media-savant/main/button.svg)](https://boboskon.github.io/media-savant/)