# Project README

## Overview
This project is a Pong game with AI, implemented in C and utilizing a custom GUI library. The game runs on Linux, Windows, web, and Wine environments.

## Features
- Basic Pong gameplay
- Single-player mode against an AI opponent
- Adjustable speed of the AI paddle
- Score tracking
- Customizable display settings (width, height)
- Debugging features

## Project Structure
```
Gui_Pong_AI/
├── build/              # .exe files produced by Main.c
├── src/
│   ├── Main.c          # Entry point
│   ├── GUI.h           # Header for GUI library functions
│   ├── GUI.c           # Implementation of GUI library functions
│   └── GameLogic.h       # Header for game logic functions
│       └── GameLogic.c   # Implementation of game logic functions
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
└── README.md           # This file
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed in specific projects:
  - Linux: X11, PNG, JPEG
  - Windows: WINAPI, X11, ALSA

## Build & Run
### Linux
```bash
cd Gui_Pong_AI/
make -f Makefile.linux all
./build/Main
```

### Windows
```bash
cd Gui_Pong_AI/
make -f Makefile.windows all
build\Main.exe
```

### Wine
```bash
cd Gui_Pong_AI/
make -f Makefile.wine all
wine build/Main.exe
```

### WebAssembly (Emscripten)
```bash
cd Gui_Pong_AI/
make -f Makefile.web all
emrun --no_browser --port 8080 build/index.html
```

# Build Steps
To build the project for a specific OS, use the appropriate Makefile. For example:
- Linux: `make -f Makefile.linux all`
- Windows: `make -f Makefile.windows all`
- WebAssembly: `make -f Makefile.web all`

To clean and rebuild:
- `make -f Makefile.(os) clean`
- `make -f Makefile.(os) all`