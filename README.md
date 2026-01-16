# CLI Audio Player
This is a minimal command-line audio player written in C++.
This project demonstrates how to load common audio formats and
play them back using the operating system's native audio APIs.
The Linux version uses ALSA and the macOS version uses AudioToolbox,
which is a framework within the Core Audio API.

## Features
- Cross-platform command-line audio playback
  - Linux: ALSA
  - macOS: AudioToolbox (Core Audio)
- Supports multiple formats through **libsndfile**
  - WAV, FLAC, OGG, AIFF, etc.
- Automatic configuration of:
  - Sample rate
  - Channel count
  - Buffer and period size
- Prints basic metadata:
  - Title
  - Track number
  - Artist
  - Album
- Simple, readable C++ design suitable for learning
  low-level audio APIs

## Building (Linux)
To build on Linux, you will need the following
libraries/tools installed:
- **CMake**
- **ALSA**
- **libsndfile**

### Debian/Ubuntu
```bash
sudo apt install libasound2-dev libsndfile1-dev
```

### Arch Linux
```bash
sudo pacman -S alsa-lib libsndfile
```

### Fedora
```bash
sudo dnf install alsa-lib-devel libsndfile-devel
```

### openSUSE
```bash
sudo zypper install alsa-devel libsndfile-devel
```

### Alpine Linux
```bash
sudo apk add alsa-lib-dev libsndfile-dev
```

### Void Linux
```bash
sudo xbps-install -S alsa-lib-devel libsndfile-devel
```

To build the audio player, simply run
```bash
cmake -B build
cd build
make
```

## Building (macOS)
To build on macOS, you will first need to install
the Xcode Command Line Tools. To do this, run
the following command:
```bash
xcode-select --install
```

You will then need to install Homebrew, which
will be used to install the dependencies. To
install Homebrew, follow the instructions
[here.](https://brew.sh/)

Next you will need the following libraries/tools
installed:
- **CMake**
- **libsndfile**

Run the following to install the libraries/tools:
```bash
brew install cmake libsndfile
```

To build the audio player, simply run
```bash
cmake -B build
cd build
make
```
