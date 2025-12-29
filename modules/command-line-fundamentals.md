<div align="center">
  <a href="https://vetswhocode.io">
    <img src="../img/vwc-logo.png" alt="Vets Who Code" width="400px" />
  </a>
</div>

<h1 align="center">Module 1: Command Line Fundamentals</h1>

**⏱ Estimated Time: 8-10 hours**

---

## Why This Matters

Every developer uses the command line. Every single one.

The command line, often referred to as the "terminal," "shell," or "CLI" (Command Line Interface), is your backstage pass to interacting with your computer in a way that goes beyond clicking and dragging. When you're deploying code, managing servers, running build tools, or using Git — you're in the terminal. Most tutorials assume you already know your way around. We're going to make sure you do.

By the end of this module, the command line will feel like home.

---

## What is the Terminal?

The terminal (also called command line, shell, or console) is a text-based interface to your computer. Instead of clicking icons and menus, you type commands.

Why would anyone choose typing over clicking?

- **Speed** — Once you know the commands, you can do things in seconds that would take minutes with a mouse
- **Power** — Some tasks can only be done from the terminal
- **Automation** — You can write scripts to do repetitive tasks for you
- **Remote access** — When you're working on servers, the terminal is often your only option

### Terminal vs Shell

Quick clarification:

- **Terminal** — The application/window you type in
- **Shell** — The program that interprets your commands

Common shells:
- **Bash** — The classic, available everywhere
- **Zsh** — Modern, powerful, default on Mac
- **PowerShell** — Windows (we recommend using Git Bash or WSL instead)

If you're on Mac, you're using Zsh by default. If you're on Linux, probably Bash. Either works fine for this course.

---

## Opening Your Terminal

### Operating Systems and Access

**Mac:**
- Press `Cmd + Space`, type "Terminal", hit Enter
- Or navigate to `Applications` > `Utilities` > `Terminal`

**Windows:**
- Install [Git for Windows](https://gitforwindows.org/) which includes Git Bash
- Or use [Windows Subsystem for Linux (WSL)](https://docs.microsoft.com/en-us/windows/wsl/install)
- Alternatively: Click `Start`, then `All Programs` > `Accessories` > `Command Prompt`

**Linux:**
- Press `Ctrl + Alt + T`
- Or find Terminal in your applications menu

---

## The Prompt

When you open the terminal, you'll see something like this:

```
username@computer:~$
```

Or on Mac with Zsh:

```
username@computer ~ %
```

This is your **prompt**. It's waiting for you to type a command.

The `~` represents your home directory. The `$` or `%` indicates you're a regular user (not root/admin).

---

## Your First Commands

### Where Am I? (Print Working Directory)

```bash
pwd
```

`pwd` stands for "print working directory." It tells you where you are in the file system.

**Output:**
```
/Users/username
```

**Windows alternative:**
```bash
cd
```

---

### What's Here? (List Directories and Files)

**Mac/Linux:**
```bash
ls
```

**Windows:**
```bash
dir
```

`ls` (or `dir` on Windows) lists the contents of the current directory.

```
Desktop    Documents    Downloads    Pictures
```

### See More Details

```bash
ls -l
```

The `-l` flag shows a "long" listing with more information:

```
drwxr-xr-x  5 username  staff   160 Jan 15 10:30 Desktop
drwxr-xr-x  8 username  staff   256 Jan 14 09:15 Documents
```

This shows permissions, owner, size, date modified, and name.

### See Hidden Files

```bash
ls -a
```

Files starting with `.` are hidden by default. The `-a` flag shows all files.

```
.  ..  .zshrc  .gitconfig  Desktop  Documents
```

### Combine Flags

```bash
ls -la
```

Shows all files with details. You'll use this constantly.

---

## Navigating the File System

### Moving Around (Changing Your Working Directory)

```bash
cd Documents
```

`cd` means "change directory." Now you're inside Documents.

```bash
pwd
```
```
/Users/username/Documents
```

### Going Back (To the Previous Directory)

```bash
cd ..
```

`..` means "parent directory" — one level up.

### Going Home

```bash
cd ~
```

Or just:

```bash
cd
```

Both take you to your home directory.

### Absolute vs Relative Paths

**Absolute path** — starts from root (`/`):
```bash
cd /Users/username/Documents/Projects
```

**Relative path** — starts from where you are:
```bash
cd Documents/Projects
```

If you're already in `/Users/username`, both commands take you to the same place.

### Quick Navigation Tips

```bash
cd -
```

Takes you to the previous directory you were in. Great for bouncing between two locations.

```bash
cd ~/Documents/Projects
```

The `~` expands to your home directory, so this works from anywhere.

---

## Working with Files and Directories

### Creating Directories

**Create a new directory called "VetsWhoCode":**

```bash
mkdir VetsWhoCode
```

Creates a directory called `VetsWhoCode`.

**Create nested directories:**

```bash
mkdir -p projects/vwc/prework
```

The `-p` flag creates parent directories as needed. This creates the entire nested structure in one command.

### Creating Files

```bash
touch index.html
```

Creates an empty file called `index.html`. If the file exists, it updates the timestamp.

### Creating Multiple Files

```bash
touch index.html style.css script.js
```

Creates all three files at once.

### Viewing File Contents

```bash
cat README.md
```

`cat` prints the entire file to the terminal. Good for short files.

```bash
less README.md
```

`less` lets you scroll through longer files. Press `q` to quit.

```bash
head -20 README.md
```

Shows the first 20 lines.

```bash
tail -20 README.md
```

Shows the last 20 lines.

### Copying Files

```bash
cp index.html backup.html
```

Copies `index.html` to a new file called `backup.html`.

```bash
cp -r projects projects-backup
```

The `-r` flag copies directories recursively (including all contents).

### Moving and Renaming

```bash
mv old-name.html new-name.html
```

Renames a file.

```bash
mv index.html ../
```

Moves `index.html` to the parent directory.

```bash
mv index.html ~/Documents/
```

Moves it to Documents.

### Deleting a Directory (Oops!)

**Mac/Linux:**

```bash
rm unwanted-file.txt
```

Deletes the file. **There is no trash. It's gone.**

```bash
rm -r unwanted-folder
```

or

```bash
rm -r NameOfDirectory
```

Deletes a directory and everything inside it.

**Windows:**

```bash
rmdir /S NameOfDirectory
```

> ⚠️ **Be careful with `rm`.** There's no undo. Double-check before you hit Enter, especially with `-r`.

### Safe Delete Practice

Before deleting, list what you're about to remove:

```bash
ls unwanted-folder
```

Then delete:

```bash
rm -r unwanted-folder
```

---

## Finding Things

### Find Files by Name

```bash
find . -name "*.html"
```

Finds all `.html` files starting from the current directory (`.`).

```bash
find ~/Documents -name "index.html"
```

Finds files named `index.html` in Documents.

### Search Inside Files

```bash
grep "function" script.js
```

Finds lines containing "function" in `script.js`.

```bash
grep -r "TODO" .
```

Recursively searches all files in the current directory for "TODO".

```bash
grep -n "error" logfile.txt
```

The `-n` flag shows line numbers.

---

## Pipes and Redirection

This is where the terminal gets powerful.

### Pipes

The pipe `|` takes the output of one command and feeds it to another.

```bash
ls -la | less
```

Lists files and sends the output to `less` so you can scroll through it.

```bash
cat logfile.txt | grep "error"
```

Shows only lines containing "error".

```bash
history | grep "git"
```

Shows your command history filtered to only git commands.

### Chaining Pipes

```bash
cat data.txt | grep "active" | wc -l
```

This:
1. Reads the file
2. Filters to lines with "active"
3. Counts the lines (`wc -l`)

### Output Redirection

```bash
ls -la > filelist.txt
```

The `>` redirects output to a file. Creates or overwrites the file.

```bash
echo "New line" >> notes.txt
```

The `>>` appends to a file instead of overwriting.

```bash
cat file1.txt file2.txt > combined.txt
```

Combines two files into one.

---

## Command History and Shortcuts

### History

```bash
history
```

Shows your recent commands.

Press `Up Arrow` to cycle through previous commands.

Press `Ctrl + R` to search your history. Start typing and it finds matching commands.

### Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + A` | Jump to beginning of line |
| `Ctrl + E` | Jump to end of line |
| `Ctrl + U` | Clear line before cursor |
| `Ctrl + K` | Clear line after cursor |
| `Ctrl + W` | Delete word before cursor |
| `Ctrl + L` | Clear the screen |
| `Ctrl + C` | Cancel current command |
| `Tab` | Auto-complete files and commands |

**Tab completion is your best friend.** Start typing a file or command name and press Tab. If there's one match, it completes. If there are multiple, press Tab twice to see options.

---

## Customizing Your Shell

### The Config File

Your shell reads a config file when it starts:

- **Zsh:** `~/.zshrc`
- **Bash:** `~/.bashrc` or `~/.bash_profile`

### Creating Aliases

Aliases are shortcuts for commands you use often. Add these to your config file:

```bash
# Open the config file
nano ~/.zshrc    # or ~/.bashrc for Bash
```

Add aliases like:

```bash
# Navigation
alias ..="cd .."
alias ...="cd ../.."
alias home="cd ~"
alias projects="cd ~/Documents/projects"

# List files
alias ll="ls -la"
alias la="ls -a"

# Git shortcuts (preview - more in Git module)
alias gs="git status"
alias ga="git add"
alias gc="git commit"
alias gp="git push"

# Safety nets
alias rm="rm -i"    # Asks for confirmation
alias mv="mv -i"    # Asks before overwriting
alias cp="cp -i"    # Asks before overwriting

# Clear screen
alias c="clear"
```

Save the file and reload:

```bash
source ~/.zshrc    # or source ~/.bashrc
```

Now `ll` works as `ls -la`, `gs` works as `git status`, etc.

### Setting Your Editor

Add this to your config file:

```bash
export EDITOR="code"    # VS Code
```

Now when programs need to open an editor, they'll use VS Code.

### Custom Prompt (Optional)

You can customize what your prompt displays. Here's a simple example:

```bash
# Shows: directory-name $
PS1="%1d $ "
```

Or with colors:

```bash
# Shows: directory-name in blue, then $
PS1="%F{blue}%1d%f $ "
```

---

## Practical Exercises

### Exercise 1: Navigation Drill

Without looking at notes, complete these tasks:

1. Open your terminal
2. Print your current directory
3. Navigate to your Documents folder
4. List all files including hidden ones
5. Go back to your home directory using the shortcut
6. Navigate to Documents using an absolute path

### Exercise 2: File Operations

1. Create a directory called `vwc-prework`
2. Inside it, create three directories: `html`, `css`, `js`
3. Inside `html`, create files: `index.html`, `about.html`, `contact.html`
4. Copy `index.html` to the parent `vwc-prework` directory
5. Rename the copy to `home.html`
6. Delete `home.html`
7. List the entire structure to verify

### Exercise 3: Finding and Searching

1. Find all `.html` files in your `vwc-prework` directory
2. Create a file with some text: `echo "Hello World" > greeting.txt`
3. Use `grep` to find "World" in that file
4. Use `cat` to display the file contents

### Exercise 4: Pipes Practice

1. List all files in your home directory and count them: `ls ~ | wc -l`
2. View your command history and filter to only `cd` commands
3. List files and save the output to a file called `my-files.txt`

### Exercise 5: Customize Your Shell

1. Open your shell config file (`~/.zshrc` or `~/.bashrc`)
2. Add at least 5 aliases that will help your workflow
3. Save and reload the config
4. Test each alias

---

## Common Mistakes and Fixes

### "Command not found"

You mistyped the command or it's not installed.

```bash
# Wrong
lss -la

# Right
ls -la
```

### "No such file or directory"

The file or path doesn't exist. Check your spelling and current location with `pwd`.

### "Permission denied"

You don't have access. For your own files, this usually means the file isn't executable. For system files, you may need `sudo` (use carefully).

### Accidentally Started Something

If a command is running and won't stop, press `Ctrl + C` to cancel it.

### Terminal Looks Broken

If your terminal looks weird (no prompt, strange characters), type:

```bash
reset
```

This restores it to normal.

---

## How to Know You're Ready

You should be able to do all of the following **from memory**, without looking anything up:

- [ ] Navigate to any directory using both relative and absolute paths
- [ ] Create nested directory structures in one command
- [ ] Create, copy, move, and delete files and directories
- [ ] View file contents using multiple methods
- [ ] Find files by name
- [ ] Search for text inside files
- [ ] Use pipes to chain commands
- [ ] Redirect output to files
- [ ] Use keyboard shortcuts for efficiency
- [ ] Set up useful aliases in your shell config

---

## Your Gate

Take a screenshot of your terminal showing:

1. Your custom aliases (run `alias` to list them)
2. Your shell config file open, showing your customizations

**This screenshot goes on your portfolio's About page.**

---

## Quick Reference

### Navigation
| Command | Description |
|---------|-------------|
| `pwd` | Print working directory |
| `ls` / `dir` | List files (Mac/Linux / Windows) |
| `ls -la` | List all files with details |
| `cd directory` | Change directory |
| `cd ..` | Go up one level |
| `cd ~` / `cd` | Go to home |
| `cd -` | Go to previous directory |

### Files and Directories
| Command | Description |
|---------|-------------|
| `mkdir name` | Create directory |
| `mkdir -p path/to/dir` | Create nested directories |
| `touch file` | Create file |
| `cp source dest` | Copy file |
| `cp -r source dest` | Copy directory |
| `mv source dest` | Move or rename |
| `rm file` | Delete file |
| `rm -r directory` / `rmdir /S` | Delete directory (Mac/Linux / Windows) |

### Viewing Files
| Command | Description |
|---------|-------------|
| `cat file` | Print entire file |
| `less file` | Scroll through file |
| `head -n file` | First n lines |
| `tail -n file` | Last n lines |

### Finding and Searching
| Command | Description |
|---------|-------------|
| `find . -name "pattern"` | Find files by name |
| `grep "text" file` | Search in file |
| `grep -r "text" .` | Search recursively |

### Pipes and Redirection
| Symbol | Description |
|--------|-------------|
| `\|` | Pipe output to next command |
| `>` | Redirect output to file (overwrite) |
| `>>` | Redirect output to file (append) |

---

**Now, you're armed with the knowledge and tools to embark on your web development journey. Get ready to create, innovate, and make your mark on the digital world! 🚀**

---

**Next up:** [Module 2: Code Editor Setup](code-editor-setup.md)
