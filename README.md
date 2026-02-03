# quickserver

A minimal static file server in bash. No dependencies, no installation, just copy and run.

## Quick Start

```bash
# Serve current directory on port 8080
./quickserver

# Serve a specific directory
./quickserver ./public

# Serve on a different port
./quickserver -p 3000 ./dist
```

## Installation

```bash
# Download
curl -O https://raw.githubusercontent.com/willc/quickserver/main/quickserver
chmod +x quickserver

# Or clone
git clone https://github.com/willc/quickserver.git
```

## Usage

```
quickserver [options] [directory]

Options:
  -p, --port PORT    Port to listen on (default: 8080)
  -v, --verbose      Show request details
  -h, --help         Show help message
  --version          Show version
```

## Features

- Serves static files with proper MIME types
- Automatic `index.html` for directory requests
- No dependencies beyond bash and netcat
- Directory traversal protection
- ~150 lines of readable bash

## Supported File Types

| Type | Extensions |
|------|-----------|
| HTML | `.html`, `.htm` |
| CSS | `.css` |
| JavaScript | `.js` |
| JSON | `.json` |
| Images | `.png`, `.jpg`, `.jpeg`, `.gif`, `.svg`, `.ico`, `.webp` |
| Fonts | `.woff`, `.woff2`, `.ttf`, `.otf` |
| Media | `.mp3`, `.mp4`, `.webm` |
| Other | `.pdf`, `.zip`, `.txt`, `.md`, `.xml` |

## Requirements

- Bash 4+
- Netcat (`nc`)

Works on macOS and Linux.

## FAQ

**Why did you make this?**

It's a handy tool for pentesters, capture-the-flag players, and general tinkerers in home labs.

**Is this production ready?**

No. This is for development, testing, and quick file sharing. Use nginx, Apache, or a proper static file host for production.

**Why doesn't it work on Windows?**

It requires bash and netcat. Use WSL if you need it on Windows.

**Can it handle multiple connections?**

One at a time. It's a ~150 line bash script, not nginx.

**Does it support HTTPS?**

No. Use a reverse proxy if you need TLS.

## License

MIT
