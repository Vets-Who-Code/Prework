Certainly! Here is the improved version of the "Windows Tooling" section focused exclusively on setting up a development environment on Windows:

<div align="center">
  <a href="https://vetswhocode.io">
    <img src="../img/vwc-logo.png" alt="Vets Who Code" width="400px" />
  </a>
</div>

<h1 align="center">Windows Tooling</h1>

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

### Install Visual Studio Code

Visual Studio Code (VSCode) is a powerful, open-source code editor available for Windows, Mac, and Linux. Install it using the following command:

```bash
winget install --id Microsoft.VisualStudioCode
```

Or download it directly from the [Visual Studio Code website](https://code.visualstudio.com/Download).

### Configure VSCode for WSL

1. **Open VSCode:** Launch Visual Studio Code.
2. **Open Terminal:** Press `Ctrl + ` to open the terminal.
3. **Open Command Palette:** Press `Ctrl + Shift + P` to open the command palette.
4. **Select Default Shell:** Type `Select Default Shell` and choose `WSL Bash` from the options.
5. **Open New Terminal:** Click on the `+` icon in the terminal window to open a new WSL Bash terminal.

### Install Essential Extensions

Enhance your VSCode experience with these essential extensions:

- **Prettier**: Code formatter.
- **ESLint**: Linting tool for JavaScript.
- **GitLens**: Supercharge the built-in Git capabilities.
- **Bracket Pair Colorizer**: Colorize matching brackets.

### Keyboard Shortcuts

Improve your productivity by mastering keyboard shortcuts. Here are some great resources for Windows shortcuts:

- [Useful Keyboard Shortcuts](https://www.reddit.com/r/AskReddit/comments/633ok7/what_are_some_useful_keyboard_shortcuts_that/)

Additionally, you can install CheatSheet for Windows alternatives to see all the shortcuts available in each application.

### Additional Tools

Consider installing the following tools to further enhance your development environment:

- **Node.js and npm:** JavaScript runtime and package manager:
  ```bash
  winget install OpenJS.NodeJS
  ```
- **Git:** Version control system:
  ```bash
  winget install Git.Git
  ```
- **Zsh and Oh My Zsh:** Improved shell and its configuration framework (optional for advanced users):
  ```bash
  winget install Zsh
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```

### Additional Resources

To make your code editor more comfortable, check out these two podcast episodes for the best tips and extensions:
- [Why is Everyone Switching to VS Code](https://syntax.fm/show/012/why-is-everyone-switching-to-vs-code)
- [VS Code Round Two](https://syntax.fm/show/048/vs-code-round-two)

The podcasts are great, but you can also read the show notes for a quick summary.

## Conclusion

With these tools and tips, you're well on your way to creating a powerful and efficient Windows development environment. Good luck, and happy coding! 🚀