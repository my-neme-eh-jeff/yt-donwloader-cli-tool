# YouTube Downloader CLI

This is a command-line interface (CLI) application written in Rust. It is designed to download YouTube videos and audio files. The application uses the `reqwest` crate for HTTP requests, `serde_json` for JSON parsing, and `std::collections::HashMap` for data storage.

## Modules

The application is divided into two modules:

1. `download`: This module handles the actual downloading of files. It takes a URL and a destination path, and downloads the file from the URL to the specified path.

2. `errors`: This module defines custom error types for the application. These error types are used throughout the application to handle various error conditions.

## Usage

To use the application, run it from the command line with the desired arguments. Here are some examples:

### Download a YouTube video in the highest quality:

```bash
download-cli -m auto -a co.wuk.sh -p /path/to/download/to -u https://www.youtube.com/watch?v=dQw4w9WgXcQ -q high -c vp9
```

Download a YouTube video in the lowest quality:
```bash
download-cli -m auto -a co.wuk.sh -p /path/to/download/to -u https://www.youtube.com/watch?v=dQw4w9WgXcQ -q low -c vp9
```

Download a YouTube video without audio:
```bash
download-cli -m auto -a co.wuk.sh -p /path/to/download/to -u https://www.youtube.com/watch?v=dQw4w9WgXcQ -q high -c vp9 -m true
```


Download a YouTube video with a specific audio format:
```bash
download-cli -m auto -a co.wuk.sh -p /path/to/download/to -u https://www.youtube.com/watch?v=dQw4w9WgXcQ -q high -c vp9 -f mp3
```

## Installation
To install the application, you need to have Rust installed on your machine. You can download Rust from the official website. After installing Rust, you can clone this repository and build the application using cargo, the Rust package manager:
```bash
git clone https://github.com/my-neme-eh-jeff/yt-donwloader-cli-tool.git yt-download-cli
cd yt-download-cli
cargo build 
```

