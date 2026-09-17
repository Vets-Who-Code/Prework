<div align="center">
  <a href="https://vetswhocode.io">
    <img src="../img/vwc-logo.png" alt="Vets Who Code" width="400px" />
  </a>
</div>

<h1 align="center">Windows Tooling</h1>

This guide provides quick setup instructions for Windows users. For detailed learning and exercises, see the **[Prework Modules](../modules/README.md)**.

Windows has significantly improved for web development, and with the right setup, you can create a powerful and efficient development environment.

## Setting Up Your Development Environment

### Install Windows Subsystem for Linux (WSL)

WSL allows you to run a Linux distribution within Windows, providing access to the same tools and terminal environment as Mac and Linux users. Follow these steps to set up WSL:

1. **Install WSL:** Open PowerShell as Administrator and run:
   ```bash
   wsl --install
   ```
   For more detailed instructions, visit the [WSL installation guide](https://docs.microsoft.com/en-us/windows/wsl/install).

2. **Choose a Linux Distribution:** Once WSL is installed, choose a Linux distribution to install (Ubuntu is recommended for beginners).

3. **Initialize Your Distribution:** Open your newly installed Linux distribution from the Start menu and complete the initial setup.

4. **Update and Upgrade:** Run the following commands to update and upgrade your distribution:
   ```bash
   sudo apt update
   sudo apt upgrade
   ```

> **Keep all your work inside Ubuntu.** Store projects in your Ubuntu home folder (`~`, e.g. `~/code`), not in `C:\Users\...` (`/mnt/c/...`). Files on the Windows side are slow to work with from Linux and can cause permission and line-ending problems.

### Install Visual Studio Code

Visual Studio Code (VSCode) is a powerful, open-source code editor available for Windows, Mac, and Linux. Install it using the following command:

```bash
winget install --id Microsoft.VisualStudioCode
```

Or download it directly from the [Visual Studio Code website](https://code.visualstudio.com/Download).

### Configure VSCode for WSL

**For complete VS Code setup instructions, see [Module 2: Code Editor Setup](../modules/code-editor-setup.md).**

1. **Install the WSL extension:** In VS Code, press `Ctrl + Shift + X`, search for **"WSL"** (by Microsoft), and click Install.
2. **Open Ubuntu:** Launch Ubuntu from the Start menu.
3. **Go to your project:** `cd` into your project folder inside your Ubuntu home folder:
   ```bash
   mkdir -p ~/code/my-project
   cd ~/code/my-project
   ```
4. **Open VS Code from Ubuntu:** Run:
   ```bash
   code .
   ```
5. **Confirm the connection:** Look at the bottom-left corner of VS Code. It should say **"WSL: Ubuntu"**. The integrated terminal (`` Ctrl + ` ``) is now an Ubuntu terminal.

### Install VetsWhoCode Extensions

The VetsWhoCode Extension Pack includes everything you need for our curriculum:

1. Open VS Code
2. Press `Ctrl + Shift + X` to open Extensions
3. Search for **"VetsWhoCode Extension Pack"**
4. Click Install

This pack includes:
- **Prettier**: Code formatter
- **ESLint**: Linting tool for JavaScript
- **GitLens**: Supercharge the built-in Git capabilities
- **Live Server**: Local development server with live reload
- **Auto Rename Tag**: Automatically rename paired HTML tags
- And more!

#### Additional VWC Extension

Also install the **Vets Who Code HashFlag Extension** to proudly display your affiliation:

1. Search for "HashFlag" in Extensions
2. Click Install

### Keyboard Shortcuts

Improve your productivity by mastering keyboard shortcuts. Here are some great resources for Windows shortcuts:

- [Useful Keyboard Shortcuts](https://www.reddit.com/r/AskReddit/comments/633ok7/what_are_some_useful_keyboard_shortcuts_that/)

Additionally, you can install CheatSheet for Windows alternatives to see all the shortcuts available in each application.

### Additional Tools

Install these **inside Ubuntu (WSL)**, not on the Windows side. Run every command below in your Ubuntu terminal:

- **Node.js and npm:** JavaScript runtime and package manager, installed with nvm:
  ```bash
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash
  # close and reopen your Ubuntu terminal
  nvm install --lts
  ```
- **Git:** Version control system:
  ```bash
  sudo apt install -y git
  ```
- **Zsh and Oh My Zsh:** Improved shell and its configuration framework (optional for advanced users):
  ```bash
  sudo apt install -y zsh
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```

### Additional Resources

To make your code editor more comfortable, check out these two podcast episodes for the best tips and extensions:
- [Why is Everyone Switching to VS Code](https://syntax.fm/show/012/why-is-everyone-switching-to-vs-code)
- [VS Code Round Two](https://syntax.fm/show/048/vs-code-round-two)

The podcasts are great, but you can also read the show notes for a quick summary.

With these tools and tips, you're well on your way to creating a powerful and efficient Windows development environment. Good luck, and happy coding! 🚀
