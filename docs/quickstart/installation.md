---
title: Installation
sidebar_position: 1
---

For the quickstart, you will need:

1. `ffmpeg` and `ffprobe` 6.x
2. GNU make
3. Optional: A text editor such as [VS Code][vs-code]

[vs-code]: https://code.visualstudio.com/

## Windows 11

1. Install [scoop][scoop-installation] if you do not already have it installed.
1. Install `ffmpeg` and `make` using scoop:
    ```bash
    scoop install ffmpeg make
    ```
1. Verify your installation by running an `ffmpeg` command and a `make` command such as the following:
    ```bash
    # Check ffmpeg version
    ffmpeg -version
    # Check the make version
    make --version
    ```

[scoop-installation]: https://scoop.sh/

## Mac OS

1. Install [Homebrew][brew-installation] if you do not already have it installed.
2. Install `ffmpeg` using Homebrew:
    ```bash
    brew install ffmpeg
    ```
1. Verify your installation works by running an `ffmpeg` command such as the following:
    ```bash
    # Check ffmpeg version
    ffmpeg -version
    ```

[brew-installation]: https://brew.sh

## Linux

1. Download the latest `ffmpeg` [static build][ffmpeg-static-build] hosted by John Van Sickle:
    ```bash
    # Create a temporary folder to save downloads
    mkdir ffmpeg-download
    cd ffmpeg-download

    # Download ffmpeg
    wget https://johnvansickle.com/ffmpeg/builds/ffmpeg-git-amd64-static.tar.xz

    # Download the MD5 and perform an integrity check
    wget https://johnvansickle.com/ffmpeg/builds/ffmpeg-git-amd64-static.tar.xz.md5
    md5sum -c ffmpeg-git-amd64-static.tar.xz.md5
    ```
1. Unzip it:
    ```
    tar xvf ffmpeg-git-amd64-static.tar.xz
    ```
1. Copy the files over to a folder in `PATH`:
    ```
    # Copy binaries over to ~/.local/bin (you may use a different place to store the binaries)
    cd ffmpeg-git-*
    cp * ~/.local/bin
    ```
1. Verify your installation works by running an `ffmpeg` command such as the following:
    ```bash
    # Check ffmpeg version
    ffmpeg -version
    ```


[ffmpeg-static-build]: https://johnvansickle.com/ffmpeg/
