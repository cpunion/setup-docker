# Setup Docker GitHub Action

This action installs Docker on GitHub Actions runners for Windows, macOS, and Linux operating systems.

## Features

- Supports Windows, macOS, and Linux
- Automatically detects the operating system and installs the appropriate Docker version
- Installs Docker Desktop on Windows and macOS
- Installs Docker Engine on Linux
- Optional version specification

## Usage

Add this to your GitHub Actions workflow:

```yaml
steps:
- uses: cpunion/setup-docker@v1
```

With specific version (optional):

```yaml
steps:
- uses: cpunion/setup-docker@v1
  with:
    version: '20.10.21'
```

## Operating System Support

- Windows: Installs Docker Desktop
- macOS: Uses Colima (Intel/x86_64 only)
  - Supported version: macOS 13 (Ventura)
- Linux: Installs Docker Engine using apt package manager

## System Requirements

- Windows: Windows 10 or later
- macOS:
  - Architecture: Intel/x86_64 only
  - Version: macOS 13 (Ventura)
- Linux: Ubuntu 20.04 or later

## License

MIT
