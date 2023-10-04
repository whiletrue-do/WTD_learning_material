---
layout: default
title: using the terminal in VSCode
parent: IDE
grand_parent: Setting up your environment
nav_order: 2
---

# Special Lesson: Using the Terminal in VSCode on macOS and Windows

This section will help you understand how to use the integrated terminal in Visual Studio Code (VSCode) and how to switch between different terminal environments on macOS and Windows.

## The integrated terminal

The integrated terminal in VSCode is a powerful tool that allows you to run shell commands directly within the editor. This is incredibly useful for tasks like running scripts, installing packages, or managing version control. On macOS and Windows, you have multiple options for your terminal environment:

### macOS

- **Terminal**: The native command-line interface for macOS.
  
- **iTerm2**: A third-party terminal that offers additional features.

### Windows

- **Command Prompt**: The native command-line interface for Windows.
  
- **PowerShell**: A more advanced command-line interface that includes scripting capabilities.
  
- **Git Bash**: Provides a set of Unix commands on a Windows machine, useful for Git operations and other tasks.

## Guide to managing your IDE Terminal

### 1. Open the Terminal in VSCode

You can open the terminal by going to `View -> Terminal` or by pressing `Ctrl + ~` on Windows or `Control + ~` on macOS.

The

### Switch Terminal Environments

To switch between different terminal environments, click on the dropdown menu next to the "New Terminal" button (`+`) in the terminal pane.

#### macOS:

- Choose `Terminal` to use the native macOS command-line interface.
- Choose `iTerm2` if you have it installed and prefer its additional features.

#### Windows:

- Choose `Command Prompt` to use the native Windows command-line interface.
- Choose `PowerShell` for a more advanced, scriptable environment.
- Choose `Git Bash` if you have it installed and prefer a Unix-like environment.

### Run Basic Commands

Try running some basic commands to get a feel for each environment.

- List files: `ls` on macOS, `dir` in Command Prompt and PowerShell, `ls` in Git Bash.
- Change directory: `cd your_folder_name` works in all environments.

### 4. Run a Python Script

Navigate to a folder containing a Python script and run it using `python script_name.py`.

### 5. Close and Reopen Terminal

You can close the terminal by clicking the trash bin icon next to the terminal dropdown. Reopen it by going to `View -> Terminal` or pressing `Ctrl + ~` on Windows or `Control + ~` on macOS.

## Resources

- [VSCode Integrated Terminal Documentation](https://code.visualstudio.com/docs/editor/integrated-terminal)
- [Windows Command Prompt vs PowerShell](https://www.howtogeek.com/163127/how-powershell-differs-from-the-windows-command-prompt/)
- [Git Bash for Windows](https://gitforwindows.org/)
- [iTerm2 for macOS](https://iterm2.com/)
