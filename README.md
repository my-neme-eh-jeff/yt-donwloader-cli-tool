# YouTube Downloader CLI

This is a command-line interface (CLI) application written in Rust for downloading YouTube videos and audio files. The application uses the `reqwest` crate for HTTP requests, `serde_json` for JSON parsing, and `std::collections::HashMap` for data storage.

## Features

- Download YouTube videos in various qualities and codecs
- Download audio-only files in different formats
- Customize download settings such as disabling TikTok watermark, dubbing language, and muting audio
- Specify custom API URL and download path

## Installation

To install the YouTube Downloader CLI, ensure you have Rust installed on your machine. You can download Rust from the official website: https://www.rust-lang.org/

Once Rust is installed, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/my-neme-eh-jeff/yt-donwloader-cli-tool.git yt-cli-downloader
   ```
2. Change to the project directory:
    ```bash
    cd yt-cli-downloader
    ```
3. Build the project:
    ```bash
    cargo build --release
    ```
The compiled binary will be located in the target/release directory.

## Usage
Use the YouTube Downloader CLI, run the application with the desired arguments. Here are some examples:

Download a YouTube video in auto mode (default settings)
```bash
cargo run -- -m auto -u "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
```
Download a YouTube video in a specific quality and codec
```bash
cargo run -- -m auto -u "https://www.youtube.com/watch?v=dQw4w9WgXcQ" -q 720p -c vp9
```

Download audio only in MP3 format
```bash
cargo run -- -m audio -u "https://www.youtube.com/watch?v=dQw4w9WgXcQ" -f mp3
```

For a full list of available options and their descriptions, please run:
```bash
cargo run -- --help
```

## Modules

The application is divided into two modules:

1. `download`: This module handles the actual downloading of files. It takes a URL and a destination path, and downloads the file from the URL to the specified path.

2. `errors`: This module defines custom error types for the application. These error types are used throughout the application to handle various error conditions.
