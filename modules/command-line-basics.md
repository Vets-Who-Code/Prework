<div align="center">
  <a href="https://vetswhocode.io">
    <img src="../img/vwc-logo.png" alt="Vets Who Code" width="400px" />
  </a>
</div>

<h1 align="center">Command Line Basics</h1>

In this module, we'll dive into the fundamentals of the command line, a powerful tool that will empower you to work your coding wizardry.

&emsp;
## :computer: What's the Command Line?

The command line, often referred to as the "command prompt," "terminal," or "CLI" (Command Line Interface), is your backstage pass to interacting with your computer in a way that goes beyond clicking and dragging. It's where the real magic happens.

### Operating Systems and Access

- **MacOS:** To access the Terminal, navigate to `Applications` > `Utilities` > `Terminal`.
- **Windows:** Click `Start`, then `All Programs` > `Accessories` > `Command Prompt`.

&emsp;
## :page_with_curl: Command Line Operations

Let's start with some essential commands to navigate this new territory:

### Print Working Directory (Where Are You?)

- **MacOS:** Type `pwd` and press Enter.
- **Windows:** Use `cd` and press Enter.

### List Directories and Files

- **MacOS:** Type `ls` and press Enter.
- **Windows:** Use `dir` and press Enter.

### Creating a New Directory

- Create a new directory called "VetsWhoCode" by typing `mkdir VetsWhoCode` and pressing Enter.

### Changing Your Working Directory

- Move into your new directory with `cd VetsWhoCode` and press Enter.

### Going Back to the Previous Directory

- To return to the previous directory, simply type `cd ..` and press Enter.

### Deleting a Directory (Oops!)

- In MacOS: `rm -r NameOfDirectory`
- In Windows: `rmdir /S NameOfDirectory`

&emsp;
## :sparkles: The Code Editor: Your Creative Playground

Now that you've got the hang of the command line, let's introduce you to your trusty sidekick: the code editor. An Integrated Development Environment (IDE) is your go-to software for writing, debugging, and deploying code. Our favorite is Visual Studio Code. [Download it here](https://code.visualstudio.com/) and supercharge it with our [VetsWhoCode Extension Pack](https://marketplace.visualstudio.com/items?itemName=VetsWhoCode.vetswhocode-extension-pack).

&emsp;
## :globe_with_meridians: Browser Matters

We recommend using Google Chrome for its powerful developer tools. [Download it here](https://www.google.com/chrome/) and embark on your web development journey.

&emsp;
## :octocat: Git and GitHub: The Developer's Playground

Git and GitHub are essential for collaboration and version control. Here's how to get started:

1. **Install Git:** Download and install Git for Windows from the official [Git website](https://git-scm.com/).

2. **Configure Git:** Open Git Bash and set your name and email using these commands:

   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "youremail@example.com"
   ```

3. **Create the repository:** Start by creating a new repository. Click "New" and follow the prompts.

   ![GitHub New Repository](https://user-images.githubusercontent.com/24581531/218554688-7d3594a4-eb28-41f2-8683-8426d2783480.png)

4. **Clone the repository:** Copy the repository URL from the "Code" button and follow these steps to clone it to your local machine:

    - Open your terminal or command prompt.
    - Run &ensp;`git clone URL-Goes-Here`

5. **Start coding:** Open the cloned repository in your favorite code editor, such as Visual Studio Code. It's just like working with a regular folder. Make changes to files, create or delete folders, and let your creativity flow.

6. **Stage your changes:** You need to let `git` know what changes you made. To add your changes to the staging area, type `git add` followed by the file name or directory you want to add. You can use `git add .` to add all the changes. To check what changes are staged you can run `git status`. In the output the file names in green are the staged changes.

<div align="center"><img src="https://user-images.githubusercontent.com/24581531/218550920-6430e103-d36d-472a-b6a2-c8445d72b338.png" /></div>

7. **Commit changes:** Once you have added your changes to the staging area, you can commit them by typing `git commit -m "<commit message>"` followed by a meaningful message describing what changes were made.

8. **Push changes:** Upload your changes to the GitHub repository by typing `git push`. If your branch isn't setup, check the output in the command line. It may have a message like `git push --set-upstream origin <branch name>`. Once you've set your upstream, you can use `git push` for all future uploads to this branch.

9. **Pull changes:** To update your local machine with changes made elsewhere, run `git pull`.

10. **Create a pull request:** If you want to suggest changes to someone else's repository, create a pull request via the "Pull request" button on their repository page.

11. **Merge your changes:** The repository owner can merge your changes by clicking the "Merge pull request" button.


&emsp;
<hr />

**Now, you're armed with the knowledge and tools to embark on your web development journey. Get ready to create, innovate, and make your mark on the digital world! 🚀**
