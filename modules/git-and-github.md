<div align="center">
  <a href="https://vetswhocode.io">
    <img src="../img/vwc-logo.png" alt="Vets Who Code" width="400px" />
  </a>
</div>

<h1 align="center">Module 3: Git & GitHub</h1>

**⏱ Estimated Time: 8-10 hours**

---

## Why This Matters

Every professional development team uses Git. Every. Single. One.

Git tracks changes to your code over time. It lets you experiment without fear, collaborate with others, and undo mistakes. GitHub hosts your code online and shows potential employers your work.

If you want to work as a developer, Git isn't optional.

---

## What is Git?

Git is a **version control system**. It keeps track of every change you make to your code.

Think of it like this:

- **Without Git:** You have one version of your file. If you break something, you have to fix it or lose your work.
- **With Git:** You have a complete history. You can go back to any previous version at any time.

Git also lets multiple people work on the same project without overwriting each other's work.

### Git vs GitHub

**Git** — The tool that runs on your computer and tracks changes.

**GitHub** — A website that hosts Git repositories online. It's where you store your code, share it with others, and collaborate.

You can use Git without GitHub, but most developers use both together.

---

## Installing Git

### Check if Git is Installed

Open your terminal and type:

```bash
git --version
```

If you see a version number, you're good. If not, install Git:

**Mac:**
```bash
xcode-select --install
```

**Windows:**
Download from [git-scm.com](https://git-scm.com/downloads) or [Git for Windows](https://gitforwindows.org/)

**Linux:**
```bash
sudo apt install git
```

### Configure Git

Tell Git who you are. This information appears in your commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

Set VS Code as your default editor:

```bash
git config --global core.editor "code --wait"
```

Verify your settings:

```bash
git config --list
```

---

## The Mental Model

Before we start typing commands, let's understand how Git thinks.

### The Three Areas

Git has three main areas where your files can live:

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  Working        │     │  Staging        │     │  Repository     │
│  Directory      │────▶│  Area           │────▶│  (.git)         │
│                 │ add │                 │commit│                 │
│  Your files     │     │  Ready to       │     │  Permanent      │
│  as you edit    │     │  commit         │     │  history        │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

**Working Directory** — Your actual files on disk. What you see in VS Code.

**Staging Area** — A holding area for changes you want to commit. You choose what goes here.

**Repository** — The permanent history. Once committed, it's saved.

### The Flow

1. You **edit** files in your working directory
2. You **stage** the changes you want to keep (`git add`)
3. You **commit** the staged changes with a message (`git commit`)
4. You **push** commits to GitHub (`git push`)

---

## Your First Repository

### Creating a Repo

Navigate to your project folder:

```bash
cd ~/Documents/projects
mkdir my-first-repo
cd my-first-repo
```

Initialize Git:

```bash
git init
```

You'll see:

```
Initialized empty Git repository in /Users/you/Documents/projects/my-first-repo/.git/
```

Git created a hidden `.git` folder. This is where it stores all the history.

### Check the Status

```bash
git status
```

This is your most-used command. It tells you:
- What branch you're on
- What files have changed
- What's staged and what isn't

Right now you'll see:

```
On branch main
No commits yet
nothing to commit (create/copy some files and use "git add" to track)
```

---

## The Basic Workflow

### Step 1: Create a File

```bash
echo "# My First Repo" > README.md
```

Check the status:

```bash
git status
```

```
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
```

Git sees the file but isn't tracking it yet.

### Step 2: Stage the File

```bash
git add README.md
```

Or to add all changes:

```bash
git add .
```

Check status again:

```bash
git status
```

```
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
```

The file is staged, ready to commit.

<div align="center"><img src="https://user-images.githubusercontent.com/24581531/218550920-6430e103-d36d-472a-b6a2-c8445d72b338.png" /></div>

### Step 3: Commit

```bash
git commit -m "Add README file"
```

The `-m` flag adds a message describing the change.

```
[main (root-commit) a1b2c3d] Add README file
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
```

### Step 4: Check the Log

```bash
git log
```

Shows your commit history:

```
commit a1b2c3d4e5f6g7h8i9j0...
Author: Your Name <your.email@example.com>
Date:   Mon Jan 15 10:30:00 2025

    Add README file
```

For a shorter view:

```bash
git log --oneline
```

---

## Staging in Detail

### Adding Files

```bash
# Add one file
git add filename.txt

# Add multiple files
git add file1.txt file2.txt file3.txt

# Add all files in current directory
git add .

# Add all HTML files
git add *.html
```

### Seeing What Changed

Before you stage, see what you've modified:

```bash
git diff
```

Shows line-by-line changes. Lines starting with `+` were added, `-` were removed.

After staging, see what will be committed:

```bash
git diff --staged
```

### Unstaging Files

Changed your mind?

```bash
git restore --staged filename.txt
```

This removes it from staging but keeps your changes in the file.

---

## Writing Good Commit Messages

Your commit messages are a record of what you did and why. Write them for your future self.

### Good Messages

```bash
git commit -m "Add navigation component with mobile menu"
git commit -m "Fix login form validation bug"
git commit -m "Update README with installation instructions"
git commit -m "Refactor user service to use async/await"
```

### Bad Messages

```bash
git commit -m "Fixed stuff"
git commit -m "WIP"
git commit -m "asdfasdf"
git commit -m "Changes"
```

### The Formula

**What** you did + **Why** (if not obvious)

Keep it under 50 characters if possible. Use present tense ("Add feature" not "Added feature").

---

## Branching

Branches let you work on different features without affecting the main code.

### The Main Branch

When you create a repo, you start on `main` (or `master` on older repos). This is your primary branch.

### Creating a Branch

```bash
git branch feature-nav
```

This creates a branch but doesn't switch to it.

### Switching Branches

```bash
git checkout feature-nav
```

Or do both at once:

```bash
git checkout -b feature-nav
```

### Seeing All Branches

```bash
git branch
```

The current branch has a `*` next to it.

### The Concept

```
main:        A──B──C
                   \
feature-nav:        D──E
```

When you branch, you get a copy of the code at that point. Changes you make on the branch don't affect `main` until you merge.

### When to Branch

- Starting a new feature
- Fixing a bug
- Experimenting with something
- Any time you're not sure your changes will work

### Branching Strategy

Branching allows you to work on different features or fixes simultaneously. Here's a basic workflow:

- **Create a New Branch:**
  ```bash
  git checkout -b <branch-name>
  ```
- **Switch to an Existing Branch:**
  ```bash
  git checkout <branch-name>
  ```
- **Merge a Branch:** First, switch to the branch you want to merge into (usually `main` or `master`), then:
  ```bash
  git merge <branch-name>
  ```

---

## Merging

When your feature is ready, you merge it back into main.

### The Process

First, switch to the branch you want to merge INTO:

```bash
git checkout main
```

Then merge your feature branch:

```bash
git merge feature-nav
```

```
Updating c3d4e5f..f6g7h8i
Fast-forward
 index.html | 10 ++++++++++
 style.css  |  5 +++++
 2 files changed, 15 insertions(+)
```

Your changes from `feature-nav` are now in `main`.

### Delete the Branch (Optional)

After merging, you don't need the feature branch anymore:

```bash
git branch -d feature-nav
```

---

## Merge Conflicts

Sometimes Git can't automatically merge changes. This happens when two branches modify the same part of a file.

### What a Conflict Looks Like

```
<<<<<<< HEAD
<h1>Welcome to My Site</h1>
=======
<h1>Hello World</h1>
>>>>>>> feature-branch
```

**Between `<<<<<<< HEAD` and `=======`** — What's in your current branch

**Between `=======` and `>>>>>>> feature-branch`** — What's in the branch you're merging

### Resolving Conflicts

1. Open the file in VS Code
2. Decide which version to keep (or combine them)
3. Delete the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
4. Save the file
5. Stage and commit:

```bash
git add filename.html
git commit -m "Resolve merge conflict in header"
```

### VS Code Help

VS Code shows conflict markers in color and gives you buttons:
- "Accept Current Change"
- "Accept Incoming Change"
- "Accept Both Changes"

Use these or edit manually.

---

## GitHub

Now let's put your code online.

### Create a GitHub Account

1. Go to [github.com](https://github.com)
2. Sign up with your email
3. Choose a professional username (employers will see this)

### Set Up SSH (Recommended)

SSH lets you push/pull without entering your password every time.

**Generate a key:**

```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
```

Press Enter to accept the default location. Add a passphrase if you want extra security.

**Start the SSH agent:**

```bash
eval "$(ssh-agent -s)"
```

**Add your key:**

```bash
ssh-add ~/.ssh/id_ed25519
```

**Copy your public key:**

Mac:
```bash
pbcopy < ~/.ssh/id_ed25519.pub
```

Windows (Git Bash):
```bash
cat ~/.ssh/id_ed25519.pub | clip
```

Linux:
```bash
cat ~/.ssh/id_ed25519.pub
# Then copy manually
```

**Add to GitHub:**

1. Go to GitHub → Settings → SSH and GPG keys
2. Click "New SSH key"
3. Paste your key
4. Save

**Test it:**

```bash
ssh -T git@github.com
```

You should see a welcome message.

---

## Connecting to GitHub

### Create a New Repo on GitHub

1. Click the `+` icon → New repository

   ![GitHub New Repository](https://user-images.githubusercontent.com/24581531/218554688-7d3594a4-eb28-41f2-8683-8426d2783480.png)

2. Name it (same as your local folder is easiest)
3. DON'T add a README (you already have one)
4. Click Create repository

### Connect Your Local Repo

GitHub shows you the commands. For an existing repo:

```bash
git remote add origin git@github.com:yourusername/your-repo.git
git branch -M main
git push -u origin main
```

**What these do:**

- `remote add origin` — Connects your local repo to GitHub
- `branch -M main` — Ensures your branch is named `main`
- `push -u origin main` — Uploads your code and sets up tracking

### Cloning an Existing Repository

If you want to work on an existing GitHub repository:

1. Copy the repository URL from the "Code" button
2. Clone it to your local machine:

```bash
git clone URL-Goes-Here
```

3. Start coding in the cloned directory

### Pushing Changes

After your initial setup, pushing is simple:

```bash
git push
```

If your branch isn't set up, check the output in the command line. It may have a message like:
```bash
git push --set-upstream origin <branch-name>
```
Once you've set your upstream, you can use `git push` for all future uploads to this branch.

### Pulling Changes

If there are changes on GitHub (from collaborators or the web interface):

```bash
git pull
```

To update your local machine with changes made elsewhere.

---

## The Complete Workflow

Here's what a typical work session looks like:

```bash
# Start your day - get latest changes
git pull

# Create a branch for your new feature
git checkout -b feature-contact-form

# Work on your code...
# (edit files, test, etc.)

# Check what you changed
git status
git diff

# Stage your changes
git add .

# Commit with a good message
git commit -m "Add contact form with validation"

# Push your branch to GitHub
git push -u origin feature-contact-form

# When ready, merge to main
git checkout main
git merge feature-contact-form

# Push main to GitHub
git push

# Delete the feature branch
git branch -d feature-contact-form
```

---

## Pull Requests

On real projects, you don't merge directly. You create a **Pull Request** (PR).

A PR is a request to merge your branch. It lets others:
- Review your code
- Comment and suggest changes
- Approve or request changes

### Creating a Pull Request

1. Push your branch to GitHub
2. Go to your repo on GitHub
3. Click "Compare & pull request" (or go to Pull Requests → New)
4. Add a title and description
5. Click "Create pull request"

### Merging a Pull Request

The repository owner can merge your changes by clicking the "Merge pull request" button.

### For Your Pre-Work

You won't need team review, but create PRs anyway to practice:

1. Push a feature branch
2. Create a PR
3. Review your own changes
4. Merge it yourself

---

## Collaborating with Teams

### Invite Collaborators

Add team members to your repository for seamless collaboration:
1. Go to repository Settings
2. Select "Collaborators"
3. Invite team members by username or email

### Code Reviews

Use pull requests for code reviews and feedback:
- Team members can comment on specific lines
- Request changes before merging
- Approve when ready

---

## GitHub Pages

Deploy your static websites directly from your GitHub repository.

### Enable GitHub Pages

1. Go to your repository Settings
2. Scroll to the "Pages" section
3. Under "Source", select the branch you want to deploy (usually `main`)
4. Select the folder (usually `/root` or `/docs`)
5. Click Save

### Access Your Site

Your site will be live at:
- `https://yourusername.github.io/repository-name`

Or if you named the repo `yourusername.github.io`:
- `https://yourusername.github.io`

### Push Your Website Code

Any changes pushed to the selected branch will automatically be deployed.

---

## GitHub Actions

Automate your workflow with GitHub Actions.

### What are GitHub Actions?

GitHub Actions allow you to automate tasks like:
- Running tests when you push code
- Deploying your application
- Checking code quality
- Building and packaging software

### Create a Workflow

1. Create a `.github/workflows` directory in your repository
2. Add a workflow file (YAML format)
3. Define your automation steps

**Example workflow** (`.github/workflows/test.yml`):

```yaml
name: Run Tests

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Run tests
        run: npm test
```

This workflow runs tests every time you push code or create a pull request.

---

## Your GitHub Profile

Your GitHub profile is a portfolio piece. Set it up well.

### Profile README

Create a special repo named exactly like your username (e.g., `jsmith/jsmith`). The README in this repo appears on your profile page.

```bash
mkdir yourusername
cd yourusername
git init
echo "# Hi, I'm Your Name 👋" > README.md
git add .
git commit -m "Add profile README"
# Create the repo on GitHub, then push
```

### What to Include

- Your name and a brief intro
- What you're learning/working on
- How to reach you
- Links to portfolio or LinkedIn

### Profile Settings

- Add a profile picture (professional)
- Fill in your bio
- Add your location
- Link to your portfolio

---

## Practical Exercises

### Exercise 1: Basic Workflow

1. Create a new directory and initialize a Git repo
2. Create an `index.html` file
3. Stage and commit it
4. Make changes to the file
5. Use `git diff` to see changes
6. Stage and commit again
7. View your commit history

### Exercise 2: Branching

1. From your repo, create a branch called `add-styles`
2. Switch to that branch
3. Create a `style.css` file
4. Commit it
5. Switch back to `main`
6. Notice `style.css` doesn't exist on `main`
7. Merge `add-styles` into `main`
8. Verify `style.css` is now on `main`

### Exercise 3: Intentional Merge Conflict

1. Create a new repo with an `index.html` containing a `<h1>` tag
2. Create a branch called `change-heading`
3. On that branch, change the `<h1>` text and commit
4. Switch back to `main`
5. Change the `<h1>` to something different and commit
6. Try to merge `change-heading` into `main`
7. Resolve the conflict
8. Complete the merge

### Exercise 4: GitHub Setup

1. Create a GitHub account (if you haven't)
2. Set up SSH authentication
3. Create a new repo on GitHub
4. Push your local repo to GitHub
5. Make a change on GitHub (edit a file through the web)
6. Pull the change to your local repo

### Exercise 5: Profile Setup

1. Create your profile README repo
2. Add content introducing yourself
3. Push it to GitHub
4. Verify it appears on your profile page
5. Complete your profile settings (photo, bio, etc.)

---

## Common Mistakes and Fixes

### "I committed to the wrong branch"

Move the commit to the right branch:

```bash
# Copy the commit hash from git log
git log --oneline

# Switch to the correct branch
git checkout correct-branch

# Cherry-pick the commit
git cherry-pick abc1234

# Go back and remove from wrong branch
git checkout wrong-branch
git reset --hard HEAD~1
```

### "I want to undo my last commit"

Keep changes but undo the commit:

```bash
git reset --soft HEAD~1
```

Undo commit AND changes:

```bash
git reset --hard HEAD~1
```

### "I made changes to the wrong file"

Discard changes to a specific file:

```bash
git restore filename.txt
```

### "I need to undo everything since last commit"

```bash
git restore .
```

### "I forgot to add something to my last commit"

```bash
git add forgotten-file.txt
git commit --amend --no-edit
```

### "My git log is too long"

Press `q` to quit the log view.

---

## How to Know You're Ready

You should be able to do all of the following without looking anything up:

- [ ] Initialize a repository
- [ ] Stage and commit files
- [ ] Write clear commit messages
- [ ] Create and switch branches
- [ ] Merge branches
- [ ] Resolve merge conflicts
- [ ] Set up a GitHub repository
- [ ] Push and pull from GitHub
- [ ] Create a pull request
- [ ] Use `git status`, `git log`, and `git diff`

---

## Your Gate

Take a screenshot of your GitHub profile showing:

1. Your profile photo and bio
2. Your contribution graph with commits
3. At least one repository

**This screenshot goes on your portfolio's About page.**

---

## Quick Reference

### Setup
```bash
git config --global user.name "Name"
git config --global user.email "email"
```

### Basic Commands
| Command | Description |
|---------|-------------|
| `git init` | Initialize a repo |
| `git status` | Check current state |
| `git add file` | Stage a file |
| `git add .` | Stage all files |
| `git commit -m "msg"` | Commit staged files |
| `git log` | View commit history |
| `git log --oneline` | Compact history |
| `git diff` | See unstaged changes |
| `git diff --staged` | See staged changes |

### Branching
| Command | Description |
|---------|-------------|
| `git branch` | List branches |
| `git branch name` | Create branch |
| `git checkout name` | Switch branch |
| `git checkout -b name` | Create and switch |
| `git merge name` | Merge branch into current |
| `git branch -d name` | Delete branch |

### Remote (GitHub)
| Command | Description |
|---------|-------------|
| `git remote add origin url` | Connect to GitHub |
| `git push` | Upload commits |
| `git push -u origin branch` | Push and track new branch |
| `git pull` | Download and merge |
| `git clone url` | Copy a repo |

### Undoing Things
| Command | Description |
|---------|-------------|
| `git restore file` | Discard changes |
| `git restore --staged file` | Unstage file |
| `git reset --soft HEAD~1` | Undo last commit, keep changes |
| `git reset --hard HEAD~1` | Undo last commit and changes |
| `git commit --amend` | Add to last commit |

---

**Next up:** [Module 4: HTML & CSS](html-css-fundamentals.md)
