# Module 2: Code Editor Setup

**⏱ Estimated Time: 4-6 hours**

---

## Why This Matters

You're going to spend hundreds of hours in your code editor. The difference between a well-configured editor and a default install is massive — we're talking hours saved over the course of the program.

VS Code is free, powerful, and industry-standard. Let's set it up right.

---

## Why Visual Studio Code?

VS Code is a powerful, open-source editor that offers a wide range of features to streamline your development process:

- **Lightweight and Fast**: Unlike some bulkier IDEs, VS Code is quick to install and load, making it perfect for both small scripts and large projects.
- **Extensible**: Customize your coding environment with a vast library of extensions available on the [VS Code Marketplace](https://marketplace.visualstudio.com/).
- **Intelligent Code Completion**: Boost your productivity with IntelliSense, which provides smart code suggestions based on your project.
- **Integrated Git**: Manage your source code versioning with ease, directly within the editor.
- **Debugging Tools**: Powerful debugging capabilities help you identify and fix issues efficiently.

---

## Installing VS Code

### Download

1. Go to [code.visualstudio.com](https://code.visualstudio.com/)
2. Download for your operating system
3. Install and open it

### First Launch

When you first open VS Code, you'll see a welcome tab. Feel free to explore, but we're going to configure everything ourselves.

---

## The Interface

Let's get oriented.

```
┌─────────────────────────────────────────────────────────────┐
│  Menu Bar                                                   │
├─────┬───────────────────────────────────────────────────────┤
│     │                                                       │
│  A  │                    Editor Area                        │
│  c  │                                                       │
│  t  │                                                       │
│  i  │                                                       │
│  v  ├───────────────────────────────────────────────────────┤
│  i  │                                                       │
│  t  │                    Panel (Terminal)                   │
│  y  │                                                       │
│     │                                                       │
├─────┴───────────────────────────────────────────────────────┤
│  Status Bar                                                 │
└─────────────────────────────────────────────────────────────┘
```

**Activity Bar** (left side) — Switch between views:
- Explorer (files)
- Search
- Source Control (Git)
- Run and Debug
- Extensions

**Editor Area** — Where you write code. Can have multiple tabs and split views.

**Panel** — Terminal, problems, output. Toggle with `` Ctrl + ` `` (backtick).

**Status Bar** (bottom) — Current file info, line/column, language mode.

---

## Essential Keyboard Shortcuts

Learn these first. They'll change how you work.

### The Most Important One

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + Shift + P` | **Command Palette** — Access any VS Code command |

The Command Palette is your gateway to everything. If you forget a shortcut, open the Command Palette and search for what you want.

### File Navigation

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + P` | Quick Open — jump to any file by typing its name |
| `Cmd/Ctrl + Tab` | Cycle through open files |
| `Cmd/Ctrl + W` | Close current file |
| `Cmd/Ctrl + \` | Split editor |

### Editing

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + D` | Select next occurrence of current word |
| `Cmd/Ctrl + Shift + L` | Select ALL occurrences of current word |
| `Alt + Up/Down` | Move line up/down |
| `Alt + Shift + Up/Down` | Copy line up/down |
| `Cmd/Ctrl + Shift + K` | Delete entire line |
| `Cmd/Ctrl + /` | Toggle comment |
| `Cmd/Ctrl + ]` | Indent line |
| `Cmd/Ctrl + [` | Outdent line |

### Multi-Cursor

| Shortcut | Action |
|----------|--------|
| `Alt + Click` | Add cursor at click location |
| `Cmd/Ctrl + Alt + Up/Down` | Add cursor above/below |
| `Cmd/Ctrl + D` | Add cursor at next occurrence |

Multi-cursor lets you type in multiple places at once. Game changer for repetitive edits.

### Search

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + F` | Find in current file |
| `Cmd/Ctrl + H` | Find and replace in current file |
| `Cmd/Ctrl + Shift + F` | Find in all files |
| `Cmd/Ctrl + Shift + H` | Find and replace in all files |

### Terminal

| Shortcut | Action |
|----------|--------|
| `` Ctrl + ` `` | Toggle terminal panel |
| `` Ctrl + Shift + ` `` | Create new terminal |
| `Cmd/Ctrl + Shift + [` | Switch between terminals |

### View

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + B` | Toggle sidebar |
| `Cmd/Ctrl + J` | Toggle panel |
| `Cmd/Ctrl + K Z` | Zen mode (distraction-free) |
| `Cmd/Ctrl + +/-` | Zoom in/out |

For a comprehensive list of shortcuts, check out the [keyboard shortcuts reference](https://code.visualstudio.com/docs/getstarted/keybindings).

---

## Required Extensions

Extensions add functionality to VS Code. Here's what you need.

### How to Install Extensions

1. Click the Extensions icon in the Activity Bar (or `Cmd/Ctrl + Shift + X`)
2. Search for the extension name
3. Click Install

### VetsWhoCode Essential Extensions

#### 1. VetsWhoCode Extension Pack

**What it does:** This pack includes essential tools and extensions tailored specifically for our curriculum. It bundles everything you need to get started.

**How to install:**
- Search for "VetsWhoCode Extension Pack" in the Extensions marketplace
- Or visit: [VetsWhoCode Extension Pack](https://marketplace.visualstudio.com/items?itemName=VetsWhoCode.vetswhocode-extension-pack)
- Click Install

---

#### 2. Vets Who Code HashFlag Extension

**What it does:** Proudly display your Vets Who Code affiliation in your projects and communications.

**How to install:**
- Search for "HashFlag" in the Extensions marketplace
- Or visit: [Vets Who Code HashFlag Extension](https://marketplace.visualstudio.com/items?itemName=OfficialVetsWhoCode.HashFlag)
- Click Install

---

### Core Development Extensions

These may be included in the VetsWhoCode Extension Pack, but are listed here for reference:

#### 3. Live Server

**What it does:** Launches a local development server with live reload. Save your file, browser refreshes automatically.

**Why you need it:** Instant feedback while building HTML/CSS/JS.

**How to use:**
- Right-click an HTML file → "Open with Live Server"
- Or click "Go Live" in the status bar

---

#### 4. Prettier - Code Formatter

**What it does:** Automatically formats your code to be consistent and readable.

**Why you need it:** Consistent formatting makes code easier to read and catches certain errors. No more arguing about tabs vs spaces.

**Setup after installing:**
1. Open Command Palette (`Cmd/Ctrl + Shift + P`)
2. Type "Preferences: Open Settings (JSON)"
3. Add these lines:

```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true
}
```

Now your code formats automatically every time you save.

---

#### 5. ESLint

**What it does:** Identifies problems in your JavaScript code — errors, bad practices, potential bugs.

**Why you need it:** Catches mistakes before you run your code. Like spell-check for JavaScript.

**Setup:** ESLint needs a configuration file in your project. We'll cover this in the JavaScript module. For now, just install the extension.

---

#### 6. Auto Rename Tag

**What it does:** When you rename an HTML tag, it automatically renames the matching closing tag.

**Why you need it:** Saves time and prevents mismatched tags.

**How it works:** Just start editing an opening tag — the closing tag updates automatically.

---

#### 7. GitLens

**What it does:** Supercharges Git inside VS Code. Shows who changed each line, when, and why.

**Why you need it:** Understanding code history is essential. GitLens makes it visible right in your editor.

**Features you'll use:**
- Hover over any line to see who last changed it
- See commit history for any file
- Compare versions side by side

---

### Recommended Extras

These aren't required but many developers find them helpful:

- **Bracket Pair Colorizer** (now built into VS Code) — Matching brackets get matching colors
- **indent-rainbow** — Makes indentation levels visually distinct
- **Material Icon Theme** — Better file icons
- **Error Lens** — Shows errors inline instead of just underlining

---

## Configuring Settings

VS Code has hundreds of settings. Here are the ones that matter.

### Opening Settings

**GUI way:** `Cmd/Ctrl + ,`

**JSON way (recommended):**
1. `Cmd/Ctrl + Shift + P`
2. "Preferences: Open Settings (JSON)"

The JSON file gives you more control and is easier to share.

### Recommended Settings

Add these to your `settings.json`:

```json
{
  // Editor basics
  "editor.fontSize": 14,
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "editor.minimap.enabled": false,
  "editor.lineNumbers": "on",
  "editor.renderWhitespace": "selection",

  // Save behavior
  "editor.formatOnSave": true,
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1000,

  // Prettier as default formatter
  "editor.defaultFormatter": "esbenp.prettier-vscode",

  // Terminal
  "terminal.integrated.fontSize": 13,

  // File explorer
  "explorer.confirmDelete": false,
  "explorer.confirmDragAndDrop": false,

  // Emmet for HTML/CSS
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  },

  // Bracket matching
  "editor.bracketPairColorization.enabled": true,
  "editor.guides.bracketPairs": true
}
```

### What These Do

| Setting | What It Does |
|---------|--------------|
| `fontSize` | Code text size |
| `tabSize` | Spaces per tab (2 is standard for web) |
| `wordWrap` | Long lines wrap instead of scrolling |
| `minimap.enabled` | Removes the code preview on the right |
| `formatOnSave` | Prettier runs when you save |
| `autoSave` | Saves files automatically |
| `bracketPairColorization` | Matching brackets share colors |

---

## Emmet: HTML Shortcuts

Emmet is built into VS Code. It lets you write HTML incredibly fast.

### Basic Syntax

Type the shortcut and press `Tab`:

```
div
```
Becomes:
```html
<div></div>
```

### Adding Classes and IDs

```
div.container
```
Becomes:
```html
<div class="container"></div>
```

```
div#main
```
Becomes:
```html
<div id="main"></div>
```

```
div.card.featured
```
Becomes:
```html
<div class="card featured"></div>
```

### Nesting

```
ul>li
```
Becomes:
```html
<ul>
  <li></li>
</ul>
```

### Multiplication

```
ul>li*5
```
Becomes:
```html
<ul>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

### Sibling Elements

```
header+main+footer
```
Becomes:
```html
<header></header>
<main></main>
<footer></footer>
```

### Adding Text

```
p{Hello World}
```
Becomes:
```html
<p>Hello World</p>
```

### Numbering

```
ul>li.item$*3
```
Becomes:
```html
<ul>
  <li class="item1"></li>
  <li class="item2"></li>
  <li class="item3"></li>
</ul>
```

### Full Page Boilerplate

```
!
```
Press Tab and you get a complete HTML5 document structure:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>

</body>
</html>
```

### Complex Example

```
nav.navbar>ul.nav-list>li.nav-item*4>a.nav-link{Link $}
```
Becomes:
```html
<nav class="navbar">
  <ul class="nav-list">
    <li class="nav-item"><a href="" class="nav-link">Link 1</a></li>
    <li class="nav-item"><a href="" class="nav-link">Link 2</a></li>
    <li class="nav-item"><a href="" class="nav-link">Link 3</a></li>
    <li class="nav-item"><a href="" class="nav-link">Link 4</a></li>
  </ul>
</nav>
```

---

## The Integrated Terminal

VS Code has a built-in terminal so you don't need to switch windows.

### Opening the Terminal

- Press `` Ctrl + ` `` (backtick, below Escape key)
- Or: View → Terminal
- Or: Command Palette → "Terminal: Create New Terminal"

### Multiple Terminals

You can have multiple terminals open:

- Click the `+` icon in the terminal panel
- Or press `` Ctrl + Shift + ` ``
- Switch between them with the dropdown or `Cmd/Ctrl + Shift + [` and `]`

### Split Terminal

Click the split icon to have two terminals side by side. Useful for running a server in one and commands in the other.

### Terminal Tips

- The terminal opens in your current workspace folder
- You can run any command you learned in Module 1
- Right-click for copy/paste options
- Utilize the terminal to run command-line tasks without leaving the editor

---

## Working with Files

### Creating Files

- Click the new file icon in the Explorer
- Or right-click → New File
- Or `Cmd/Ctrl + N` for a new untitled file

### Opening Folders

Always open a **folder** in VS Code, not individual files.

- File → Open Folder
- Or drag a folder onto VS Code
- Or from terminal: `code .` (opens current directory)

### The File Explorer

- **Single-click** a file to preview it (italicized tab)
- **Double-click** to open it for editing (regular tab)
- Drag files to move them
- Right-click for more options
- Keep your workspace organized using VS Code's file explorer and search functionality

### Go to Definition

With your cursor on a function or variable name:

- `F12` — Go to where it's defined
- `Alt + F12` — Peek at the definition without leaving your file
- `Shift + F12` — Find all references

---

## Customizing Your Workspace

### Themes

Personalize your editor with themes that suit your workflow:

1. Open Command Palette (`Cmd/Ctrl + Shift + P`)
2. Type "Preferences: Color Theme"
3. Browse and select your preferred theme

### Settings Sync

Keep your settings consistent across machines:

1. Click the gear icon in the bottom left
2. Select "Turn on Settings Sync"
3. Sign in with GitHub or Microsoft account
4. Your settings, extensions, and keybindings will sync automatically

---

## Practical Exercises

### Exercise 1: Shortcut Drill

Open VS Code and complete these tasks using only keyboard shortcuts:

1. Open the Command Palette
2. Open a new file
3. Type some text, then select all occurrences of a word
4. Open the integrated terminal
5. Close the terminal
6. Toggle the sidebar
7. Split the editor into two panes

### Exercise 2: Extension Setup

1. Install the VetsWhoCode Extension Pack
2. Install the Vets Who Code HashFlag Extension
3. Verify each core extension is working:
   - Create an HTML file and use Live Server
   - Write some messy code and watch Prettier fix it on save
   - Rename an HTML tag and watch Auto Rename Tag work

### Exercise 3: Settings Configuration

1. Open Settings (JSON)
2. Add the recommended settings from this guide
3. Customize any values you want (font size, etc.)
4. Verify formatOnSave is working

### Exercise 4: Emmet Practice

Create an HTML file and use Emmet to build:

1. A complete page structure (use `!`)
2. A navigation with 5 links
3. A main section with 3 article cards, each containing an h2 and p
4. A footer with a paragraph and a list of 3 social links

Do this without typing a single `<` or `>` — Emmet only.

### Exercise 5: Terminal Integration

1. Open a folder in VS Code
2. Open the integrated terminal
3. Create a new directory called `test`
4. Create 3 files inside it using terminal commands
5. Navigate around using the terminal
6. Verify the files appear in the Explorer

---

## Common Issues and Fixes

### "Format on Save Not Working"

1. Check that Prettier is installed
2. Verify `editor.formatOnSave` is `true` in settings
3. Check that Prettier is set as default formatter
4. Some files need a `.prettierrc` config — try creating one with `{}`

### "Emmet Not Working"

1. Make sure you're in an HTML file (check bottom right of status bar)
2. Make sure you're pressing Tab, not Enter
3. Check Emmet is enabled in settings

### "Can't Open Folder in Terminal"

To use `code .` from the terminal:
1. Open Command Palette
2. Search "Shell Command: Install 'code' command in PATH"
3. Restart your terminal

### "Extensions Not Appearing"

1. Restart VS Code
2. Check you don't have conflicting extensions
3. Try disabling and re-enabling the extension

---

## How to Know You're Ready

You should be able to do all of the following without looking anything up:

- [ ] Navigate VS Code using keyboard shortcuts
- [ ] Use the Command Palette to access features
- [ ] Install and configure extensions
- [ ] Modify settings through the JSON file
- [ ] Use Emmet to quickly write HTML
- [ ] Work efficiently with the integrated terminal
- [ ] Use multi-cursor editing
- [ ] Find and replace text across files

---

## Your Gate

Take a screenshot of your VS Code showing:

1. Your extensions list with VetsWhoCode Extension Pack and HashFlag installed
2. A sample HTML file demonstrating your workflow

**This screenshot goes on your portfolio's About page.**

---

## Quick Reference

### Keyboard Shortcuts

| Action | Windows/Linux | Mac |
|--------|---------------|-----|
| Command Palette | `Ctrl + Shift + P` | `Cmd + Shift + P` |
| Quick Open | `Ctrl + P` | `Cmd + P` |
| Toggle Terminal | `` Ctrl + ` `` | `` Ctrl + ` `` |
| Toggle Sidebar | `Ctrl + B` | `Cmd + B` |
| Find | `Ctrl + F` | `Cmd + F` |
| Find in Files | `Ctrl + Shift + F` | `Cmd + Shift + F` |
| Multi-Select | `Ctrl + D` | `Cmd + D` |
| Move Line | `Alt + Up/Down` | `Alt + Up/Down` |
| Delete Line | `Ctrl + Shift + K` | `Cmd + Shift + K` |
| Comment | `Ctrl + /` | `Cmd + /` |

### Emmet Cheatsheet

| Shortcut | Output |
|----------|--------|
| `!` | HTML5 boilerplate |
| `div.class` | `<div class="class"></div>` |
| `div#id` | `<div id="id"></div>` |
| `ul>li*3` | ul with 3 li children |
| `div+p` | div followed by p (siblings) |
| `p{text}` | `<p>text</p>` |
| `.item$*3` | 3 divs with classes item1, item2, item3 |

---

**Next up:** [Module 3: Git & GitHub](03-git.md)
