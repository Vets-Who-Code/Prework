# Windows Tooling

While you can (and many do) use Windows for web development, unless you're developing dot-net apps in Visual Studio (not the same as Visual Studio Code), you'll be saving yourself a lot of heartache if you install Linux as an app within Windows, and utilize the tools that provides for you, instead (Even Microsoft thinks so, and provides an explanation as to why [here](https://docs.microsoft.com/en-us/windows/wsl/faq#why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows). You'll still be able to run VS Code as you would in a Windows environment, but with the added bonus of being to work within the same terminal environment as Mac and Linux users, in other words, the tools that the open-source community was founded on and still uses primarily to this day.

### Windows 10 Users: #

If you are on Windows 10, this is a lot easier to accomplish than you may think.

1. The first thing you'll want to do is install Windows Subsystem for Linux... instructions to do so may be found [here](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
2. Follow the instructions to install WSL and the Linux distribution of your choice... Ubuntu is recommended if you've never used Linux before.
3. Once your distribution is initialized, you'll be able to pull up a Linux terminal (it will look a lot like a Windows Command Prompt, but will run the BASH terminal environment. For more on BASH, click [here](https://tutorials.ubuntu.com/tutorial/command-line-for-beginners#0).
4. As an added bonus, Git, the version-control system you'll be learning in this course, is the program that Linus Torvalds (creator of Linux) uses as well, and every version of Linux comes with it, pre-installed.
5. Next, download and install [VSCode](https://code.visualstudio.com/Download). VSCode is the development environment you'll be learning to use throughout the course, and is the preferred environment for many professional developers. It's available to Windows, Mac and Linux users (you'll be downloading the Windows version).

After you have Linux and VSCode installed, follow these instructions to set up VSCode to run WSL Linux & BASH (that is, the terminal) directly from VSCode:
Enable Windows Subsystem for Linux on your Windows 10 machine.

1. Open Visual Studio Code and press and hold `` Ctrl + ` `` to open the terminal.
2. Open the command palette using `Ctrl + Shift + P`.
3. Type - `Terminal: Select Default Profile`.
4. Select WSL Bash from the options.
5. Click on the + icon in the terminal window. The new terminal now will be a WSL Bash terminal!
*these instructions are credited to [stackoverflow.com](http://stackoverflow.com) user [therobinkin](https://stackoverflow.com/users/3814251/therobinkim) in his [answer](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal#answer-56225296) to this [question](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal)*

### Pre-Windows 10 Users: #
If you are not on Windows 10 (that is, you have not purchased a new computer in over 6 years), don't fret. You may not have access to WSL, but you can still get much of the same goodness by installing [Git Bash](https://gitforwindows.org/). For Win8 & below, skip steps 1-4 of the Windows 10 instructions above and install Git Bash from the download link on the GitForWindows website instead. Afterwards, proceed with step 5 and install VSCode. Setting up Git Bash in VSCode is identical to the process of setting up WSL Bash in VSCode, with the obvious exception being that you'll select 'Git Bash' as your default terminal, instead of 'WSL Bash'

You do __NOT__ need to install a new terminal program, VSCode comes with this functionality built-in, and in most regards, their built-in terminal is superior to any other one you might install separately. However, should you feel the need later on, [cmder](https://cmder.net) comes highly recommended. (Again... you __DO NOT *NEED*__ this, it's NOT required. Don't install it unless you feel the internal terminal is bogging down VSCode too much, take time to get used to that one first, and for your own sanity's sake, do not install the full version if you already went through the instructions above, which you should have by the time you're reading this).

Now I'm sure you want to make your code editor more comfy, so checkout these two podcast episodes [here](https://syntax.fm/show/012/why-is-everyone-switching-to-vs-code) and [here](https://syntax.fm/show/048/vs-code-round-two) for the best tips and extensions out there. The podcast is great, but you can just read the show notes.

For Windows, check out this Reddit [thread](https://www.reddit.com/r/AskReddit/comments/633ok7/what_are_some_useful_keyboard_shortcuts_that/).
