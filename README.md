# Music

A single-file, browser-based music player for your local library. Point it at a folder of audio files and it plays them entirely client-side — no server, no account, no upload.

## Overview

`index.html` is the whole app: HTML, CSS, and JavaScript in one file, with no build step and no dependencies to install. It uses the [File System Access API](https://developer.mozilla.org/en-US/docs/Web/API/File_System_Access_API) to read a folder you choose, reads ID3/metadata tags client-side via [jsmediatags](https://github.com/aadsm/jsmediatags), and never sends your files anywhere.

## Features

- Grid and list views of your library, with search across title/artist/album
- Full playback controls: shuffle, repeat (off/all/one), seek, skip ±15s, variable speed
- Loved songs and custom playlists, persisted in `localStorage`
- Synced lyrics view (reads a matching `.lrc` file next to a track)
- Album-art-driven background color accent

## Requirements

- A Chromium-based browser (Chrome or Edge) — the File System Access API isn't available in Firefox or Safari
- A local folder of `.mp3`, `.m4a`, `.flac`, `.aac`, or `.ogg` files (optionally with matching `.lrc` lyric files)

## Usage

Open `index.html` directly in Chrome or Edge (double-click it, or drag it into the browser), click **Open Music Folder**, and grant access to the folder containing your music. Your library loads and plays entirely in the browser — nothing is uploaded or transmitted.

Serving it over a local static server (e.g. `npx serve .`) also works and is otherwise equivalent.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).
