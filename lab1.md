# Lab Report 1

This tutorial contains instructions on how to download VScode, access a remote server, and test some commands on the remote server.



## Step 1: VS Code Download

To begin, visit the download link to download and install the current release. Click the correct installer for your OS and follow the installer's instructions.

[Visual Studio Code](https://code.visualstudio.com/Download)

Opening a new window should look similar to this.

![vscodescreen](https://user-images.githubusercontent.com/122492228/212778791-fe5bbeba-35cc-4bcf-9c88-68f7e6aaaa01.png)




## Step 1.5: Downloading Git

Windows users will need to download Git in order to use the Git Bash terminal.

[Git](https://git-scm.com/download/win)

Run the installer with default settings, then go back to VS Code and open the command palette using `Ctrl + Shift + P`. Search for "select default profile", select Git Bash, and then open a new terminal using `Ctrl + backtick`. The new terminal should be a bash terminal that looks similar to the following.

![bashscreen](https://user-images.githubusercontent.com/122492228/212781290-77c11689-9371-467c-ab3e-ebc3d7af6873.png)




## Step 2: Accessing a Remote Server from the Terminal

With the bash terminal open, type the following into your terminal, omitting the `$`.

    $ ssh cs15lwi23xyz@ieng6.ucsd.edu

Replace `xyz` with the unique characters pertaining to your user account. As this is your first time accessing the remote server, it will ask if you wish to continue connecting. Type `yes` and it will return a prompt for your password. Type in your account's password and hit enter/return. 

When you are successfully logged into the remote server, the terminal should look like this.

![remotelogin](https://user-images.githubusercontent.com/122492228/212782277-553eed8e-c324-4c71-addd-70696288e982.png)




## Step 3: Using Terminal Commands
One command you can use is ...

