# Subtitle Sync

> A clean, browser-based tool for fixing SRT subtitle timing -- no installs, no server, no data leaves your machine.

**[Open the app](https://cr4zysh4rk.github.io/subtitle-sync)**

---

## What it does

If your subtitles are out of sync with the video -- appearing too early or too late -- Subtitle Sync lets you shift all timestamps by an exact offset in seconds and download the corrected file instantly.

Everything runs in your browser. Your subtitle files are never uploaded anywhere.

---

## Screenshots

### Single File Mode
![Single file mode](docs/screenshot_single.png)

### Batch Mode -- Process a whole folder at once
![Batch mode](docs/screenshot_batch.png)

---

## Features

| Feature | Details |
|---|---|
| **Single file** | Upload one `.srt`, apply an offset, download the fixed file with its original name |
| **Batch folder** | Select a folder -- only `.srt` files are picked up, all processed with the same offset, and bundled into a ZIP |
| **Delay or advance** | Choose whether to push subtitles later (delay) or earlier (advance) |
| **Zero installs** | Runs entirely in the browser -- no Python, no ffmpeg, no command line |
| **Privacy-first** | Files never leave your machine |

---

## Usage

### Single File

1. Open the app and stay on the **Single File** tab
2. Drag and drop an `.srt` file onto the upload area, or click to browse
3. Set the offset in seconds (e.g. `6.5`)
4. Choose **Delay** (subtitles appear too early) or **Advance** (subtitles appear too late)
5. Click **Apply & Download** -- the corrected file downloads with its original filename

### Batch Folder

1. Switch to the **Batch** tab
2. Click **Select Folder** and pick a folder containing `.srt` files
3. Set the offset and direction
4. Click **Process & Download ZIP** -- all corrected files are bundled into a single ZIP

---

## Run locally

No build step needed. Just open `index.html` in any modern browser:

```
git clone https://github.com/Cr4zySh4rk/subtitle-sync.git
cd subtitle-sync
open index.html   # or double-click the file
```

---

## Tech stack

- Vanilla HTML, CSS, JavaScript -- no framework
- [JSZip](https://stuk.github.io/jszip/) for client-side ZIP generation (batch mode)
- Hosted on GitHub Pages
