# Lab Report 2

This tutorial contains instructions on how to download VScode, access a remote server, and test some commands on the remote server.



## Step 1: VS Code Download

To begin, visit the download link to download and install the current release. Click the correct installer for your OS and follow the installer's instructions.

[Visual Studio Code](https://code.visualstudio.com/Download)

Opening a new window should look similar to this.

![vscodescreen](https://user-images.githubusercontent.com/122492228/212778791-fe5bbeba-35cc-4bcf-9c88-68f7e6aaaa01.png)




## Step 1.5: Downloading Git

Windows users will need to download Git in order to use the Git Bash terminal.

[Git](https://git-scm.com/download/win)

Run the installer with default settings, then go back to VS Code and open the command palette using `Ctrl + Shift + P`. Search for "select default profile", select Git Bash, and then open a new terminal using ``Ctrl + ` ``. The new terminal should be a bash terminal that looks similar to the following.

![bashscreen](https://user-images.githubusercontent.com/122492228/212781290-77c11689-9371-467c-ab3e-ebc3d7af6873.png)




## Step 2: Accessing a Remote Server from the Terminal

With the bash terminal open, type the following into your terminal, omitting the `$`. Replace `xyz` with the unique characters pertaining to your user account.

    $ ssh cs15lwi23xyz@ieng6.ucsd.edu

As this is your first time accessing the remote server, it will ask if you wish to continue connecting. Type `yes` and it will return a prompt for your password. Type in your account's password and hit enter/return. 

When you are successfully logged into the remote server, the terminal should look like this.

![remotelogin](https://user-images.githubusercontent.com/122492228/212782277-553eed8e-c324-4c71-addd-70696288e982.png)




## Step 3: Using Terminal Commands

Now you can test out some basic Unix commands on the remote computer. 

- `ls` will **list** the files in the current directory
- `pwd` will **print** the current **working directory**
- `cd` plus `..` or the name of a directory will **change** the current **directory**
- `mkdir` will **make** a new directory
- `cp` will **copy** a file
- `rm` will **remove** a file
- `exit` will **exit** your connection to the remote server

![commands](https://user-images.githubusercontent.com/122492228/212788370-e728b6ef-c97c-41c3-89b7-6f4456f2a2a0.png)

In the example above, we used `mkdir` to make a new directory called `hello`. Then, we moved into that directory using `cd`. Using `ls` while in `hello` yielded nothing as the directory was just created. 

Later, after using `cd ..` to get back to the original directory, adding `-lat` as a modifier to `ls` let us see hidden files and their timestamps. Lastly, we used `rm` to remove the text file we copied earlier.

When you are done testing out commands and combinations, use `exit` to disconnect from the server.
