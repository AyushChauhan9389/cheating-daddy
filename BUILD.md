# How to Build Cheating Daddy

This guide explains how to build the application for your platform.

## Prerequisites

*   **Node.js**: Ensure you have Node.js installed (LTS version recommended).
*   **Git**: To clone the repository.

## Installation

1.  Clone the repository (if you haven't already):
    ```bash
    git clone https://github.com/yourusername/cheating-daddy.git
    cd cheating-daddy
    ```

2.  Install dependencies:
    ```bash
    npm install
    ```

## Running in Development

To start the application in development mode:

```bash
npm start
```

## Building the Application

The project uses [Electron Forge](https://www.electronforge.io/) for packaging and distribution.

### Build and Package (Create Executable)

To package the application for your current platform (macOS, Windows, or Linux) without creating a full installer:

```bash
npm run package
```

The output will be in the `out/` directory.

### Create Installers (Make)

To create distributable installers (e.g., `.dmg`, `.exe`, `.deb`, `.rpm`, `.zip`):

```bash
npm run make
```

The output artifacts will be in the `out/make/` directory.

### Platform Specifics

*   **macOS**: The `npm run make` command will generate a `.dmg` and/or `.zip` file if you are running on macOS.
*   **Windows**: The `npm run make` command will generate a `.exe` installer (Squirrel) and a `.zip` file if you are running on Windows.
*   **Linux**: The `npm run make` command will generate `.deb`, `.rpm`, or `.zip` files depending on your configuration and installed tools.

## Troubleshooting

*   If you encounter errors related to native modules, try running `npm rebuild` or ensure you have the necessary build tools installed for your platform (e.g., Xcode Command Line Tools for macOS, Visual Studio Build Tools for Windows, `build-essential` for Linux).
