---
title: "How to install and use Git on Windows"
tags: ""
---

By default, Git is installed on Linux and macOS computers as a command line option. However, Microsoft Windows does not include a Git command. Below are the steps on how to install and use Git and GitHub on Microsoft Windows.

### Installing Git on Windows

1.  Open the Git website.
2.  Click the Download link to download Git. The download should automatically start.
3.  Once downloaded, start the installation from the browser or the download folder.
4.  In the Select Components window, leave all default options checked and check any other additional components you want installed.
5.  Next, in the Choosing the default editor, used by Git unless you're familiar with Vim we highly recommend using a text editor you're comfortable using. If Notepad++ is installed, we suggest using it as your editor. If Notepad++ is not installed, you can cancel the install and install Notepad++ and then restart the GitHub install.
6.  Next, in the Adjusting your PATH environment, we recommend keeping the default Use Git from the command line and also from 3rd-party software as shown below. This option allows you to use Git from either Git Bash or the Windows Command Prompt.
7.  Next in the, we recommend leaving the default selected as Use OpenSSH.
8.  Next, in Choosing HTTPS transport backend, leave the default Use the OpenSSL library selected.
9.  In the Configuring the line ending conversions, select Checkout Windows-style, commit Unix-style line endings unless you need other line endings for your work.
10. In the Configuring the terminal emulator to use with Git Bash window, select Use MinTTY (the default terminal of MSYS2).
11. On the Configuring extra options window, leave the default options checked unless you need symbolic links.
12. Click the Install button
13. Once completed, you can check the option to Launch Git Bash if you want to open a Bash command line or, if you selected the Windows command line, run Git from the Windows command line.

### Configuring and connecting to a remote repository

In our example, we're using GitHub as a storage for our remote repository. Below are the steps on how you can connect to a GitHub repository. If you are new to GitHub, see: How to create a GitHub repository.	

1.  From the command line, move to the directory you want to contain your Git repository.
2.  Type the following command to configure your Git username, where <your name> will be your GitHub username.
    > git config --global user.name "<your name>"
3.  After entering the above command, you'll be returned to the command prompt. Next, enter your e-mail address by typing the following command, where <your e-mail> is your e-mail address.
    > git config --global user.email "<your e-mail>"
4.  Once the above steps are completed, you'll be ready to connect to a remote repository. To find the repository address, go to a repository on GitHub and click the Clone or download repository link to get the address. For example, we've created a repository called "example" at <https://github.com/Computerhope/example.git> address. Copy the address to your clipboard.
5.  Once copied go back to the command line and type the following command, where <URL> is the address you copied. To paste that address into the command line right-click in the command line window and click paste.
    > git clone <URL>
6.  Once the Git repository is created, you'll have a new directory in your current directory with the name of the Git repository.
7.  Once the Git remote repository is cloned to your local repository, a new folder in the current directory should appear with the name of the Git repository. For example, in our "example" Git we would have a new directory called "example". Use the cd command to change into the new directory.
8.  Once in the new directory, type the following command to list the remote repositories.
    > git remote
9.  If successful, the output is "origin," which is a special name that refers to the remote repository.
10. To see the aliases (URL or path), type the following command.
    > git remote -v

### Working in your local repository and pushing files

    >start notepad example.txt
    >git status
    >git add example.txt
    >git commit -m "First example"
    >git push

If you're working with a lot of other people, we'd recommend you pull (explained below) before committing. If your local repository is not the same as the remote repository (excluding your new changes), the commit fails. For example, if someone has added new files to the remote repository while you've been working and you try commit, it fails until you pull.

### Pulling or fetching updates from the remote repository

    If it's been awhile since you've committed any work, perform the git pull command to get the latest updates from the remote repository and merge them into your local repository. By pulling updates from a repository before committing, it verifies your local repository and the remote repository are the same and prevents merge conflicts.

    To get all changes without merging, run the git fetch command to grab all of the latest updates from the remote repository without merging changes.
