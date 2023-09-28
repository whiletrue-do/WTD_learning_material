---
layout: default
title: Windows
parent: Installing Python
grand_parent: Setting up your environment
nav_order: 2
---

# Installing Python on Windows

This guide will walk you through two methods of installing Python on Windows:

1. Installing from the official Python website.
2. Installing via Visual Studio Code (VSCode).

## Installing from the official Python website

### Step-by-step Instructions:

**Visit the Python Downloads Page**
   - Go to [Python's official download page](https://www.python.org/downloads/).

**Download the Installer**
   - Click on the "Download Python x.x.x" button (where x.x.x is the latest version).
   - This will download the executable installer for Windows.

**Run the Installer**
   - Navigate to your downloads folder and double-click on the downloaded file.
   - Ensure the checkbox for "Add Python x.x to PATH" is checked. This will make it easier to run Python from the command line.
   - Click on "Install Now".

**Verify Installation**
   - Open a new Command Prompt.
   - Type `python --version` and press Enter. You should see the version of Python you installed.

## Installing via Visual Studio Code (VSCode)

### Prerequisites:

- Ensure you have Visual Studio Code installed. If not, download it from [VSCode's official website](https://code.visualstudio.com/).

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