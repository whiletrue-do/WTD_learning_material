---
layout: default
title: linux & Mac
parent: Installing Python
grand_parent: Setting up your environment
nav_order: 1
---

## Installing Python on macOS

### Installing from the official Python website

**Visit the Python Downloads Page**
   - Go to [Python's official download page](https://www.python.org/downloads/).

**Download the macOS Installer**
   - Click on the "Download Python x.x.x" button for macOS (where x.x.x is the latest version).
   - This will download the macOS installer package.

**Run the Installer**
   - Navigate to your downloads folder and double-click on the downloaded `.pkg` file.
   - Follow the on-screen instructions to complete the installation.

**Verify Installation**
   - Open a new Terminal.
   - Type `python3 --version` and press Enter. You should see the version of Python you installed.

## Installing Python on Linux

### 1. Installing using the package manager

**Open a Terminal**

**Update package lists**

   ```bash
   sudo apt update
   ```

**Install Python**

   ```bash
   sudo apt install python3
   ```

**Verify Installation**

   ```bash
   python3 --version
   ```

You should see the version of Python you installed.

## 3. Installing via Visual Studio Code (VSCode) on Linux & Mac

### Prerequisites:

Ensure you have Visual Studio Code installed. If not, download it from [VSCode's official website](https://code.visualstudio.com/).

**Open VSCode**
   - Launch Visual Studio Code.

**Install the Python Extension**
   - Go to the Extensions view by clicking on the square icon on the sidebar or pressing `Ctrl+Shift+X`.
   - Search for "Python" and install the one published by Microsoft.

**Open the Command Palette**
   - Press `Ctrl+Shift+P` to open the command palette.

**Install Python using the Command Palette**
   - Type "Python: Select Interpreter" and select it from the dropdown.
   - If no Python interpreter is found, you'll be prompted to install one. Click on "Install" when prompted.

**Verify Installation**
   - Open a new terminal in VSCode by clicking on `Terminal > New Terminal`.
   - In the terminal, type `python --version` and press Enter. You should see the version of Python you installed.