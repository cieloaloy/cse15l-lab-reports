# Lab Report 4

This tutorial contains instructions on how to clone a repo, edit a file, and commit/push changes all from the command line.


## Setup

Before starting the activity, make sure you have a fork of the repository on your Github account.

[Lab 7 Repo](https://github.com/ucsd-cse15l-w23/lab7.git)


## Step 1: Log into ieng6

In Lab 3, we investigated and tested a LinkedList implementation, among other things. However, the code was incredibly buggy. To rectify this, we tested the code using JUnit. The following append method works, but not all of the time.

Why did the first test fail? Upon reaching the third call to append, the program continued indefinitely due to the while loop infinitely checking a non-null `n.next`. Because the second test only appended twice, it never reached this infinite state.

![output](https://user-images.githubusercontent.com/122492228/218622205-1c5eff2a-f0f8-4025-b444-c7992d95a27b.png)

There we go! This new implementation passed both tests and correctly appended an item to the LinkedList. Taking the creation of `n.next` outside of the loop allowed the loop to accurately traverse to the end of the list without stalling the program.


## Step 2: Clone the Repo

Lab 3 greatly assisted in my understanding of running JUnit tests from the command-line instead of the built-in way using VS Code. It is really helpful and clear to see a list of the failed tests and which lines caused errors without additional bits and bobs strewn on, like it would show when using the IDE's debugger.


## Step 3: Run the JUnit tests

Lab 3 greatly assisted in my understanding of running JUnit tests from the command-line instead of the built-in way using VS Code. It is really helpful and clear to see a list of the failed tests and which lines caused errors without additional bits and bobs strewn on, like it would show when using the IDE's debugger.


## Step 4: Edit the file, fixing the bug

Lab 3 greatly assisted in my understanding of running JUnit tests from the command-line instead of the built-in way using VS Code. It is really helpful and clear to see a list of the failed tests and which lines caused errors without additional bits and bobs strewn on, like it would show when using the IDE's debugger.


## Step 5: Run the JUnit tests again

Lab 3 greatly assisted in my understanding of running JUnit tests from the command-line instead of the built-in way using VS Code. It is really helpful and clear to see a list of the failed tests and which lines caused errors without additional bits and bobs strewn on, like it would show when using the IDE's debugger.


## Step 6: Commit and push changes

Lab 3 greatly assisted in my understanding of running JUnit tests from the command-line instead of the built-in way using VS Code. It is really helpful and clear to see a list of the failed tests and which lines caused errors without additional bits and bobs strewn on, like it would show when using the IDE's debugger.
