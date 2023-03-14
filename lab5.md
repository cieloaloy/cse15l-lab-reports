# Lab Report 5

This report is a retrospective on Week 6's activity about grading scripts.


## Testing Script on List Methods using implementations of ListExamples

![Screenshot 2023-03-13 211956](https://user-images.githubusercontent.com/122492228/224892594-667ed0ca-b1ad-46c0-a2d9-79b23c3476e3.png)

I used nano to edit the script that my lab partner and I worked on. Our first implementation had bugs in calculating the number of tests run and passed, so I addressed those and then tested the script using three of the given impelementations and our own JUnit tester. As expected the original implementation results in two failures, the corrected implementation results in no failures, and the compile-error implementation does not compile and instead produces the rather harsh error message.

## Step 2: Clone the Repo

![Screenshot_20230226_073526](https://user-images.githubusercontent.com/122492228/221473766-9f6d30ec-f21c-40f7-99fb-c8707fb08c8b.png)

I navigated back to the repo page and pressed the copy button (the two layered squares) next to the SSH link in order to copy it to my clipboard.
Then, back in the terminal, I typed `git clone <Ctrl>V <Enter>`to clone the link that I pasted in.

![Screenshot_20230226_073726](https://user-images.githubusercontent.com/122492228/221473974-af6b7c31-4430-4f4c-b77a-885f98d54243.png)

Before being able to compile and run the files, I made sure to `cd lab7` into the newly added directory.


## Step 3: Run the JUnit tests

![Screenshot_20230226_082548](https://user-images.githubusercontent.com/122492228/221474106-22625fd2-a8eb-4eb0-ba23-afc7b45e2fdb.png)

I visited the CSE 15L website, highlighted the first command in yellow, and pressed `<Ctrl>C` to copy it. 
Then I went back to the terminal and pressed `<Ctrl>V <Enter>` to paste and run it. 
Similarly, I went back to the website, highlighted the second command in yellow, and pressed `<Ctrl>C` to copy it. 
I went back to the terminal and typed `<Ctrl>V ListExamplesTests <Enter>` to paste and run it specifically using the ListExamplesTests file.

![Screenshot_20230226_080522](https://user-images.githubusercontent.com/122492228/221474489-555f1e47-a5c2-47f9-bf92-1c17dec95414.png)

## Step 4: Edit the file, fixing the bug

I typed `nano ListExamples <Enter>` to open the bugged file in the nano editor. After entering the nano editor, I held down `<down>` for 42 lines and held down `<right>` to navigate to the right by 12 characters. I used `<backspace>` to delete the "1" in "index1" and typed `2` in order to fix the bug.

![Screenshot_20230226_080719](https://user-images.githubusercontent.com/122492228/221474561-5f52ccce-0a61-4108-b709-e5457ffa2774.png)

To save the file, I pressed `<Ctrl>O <Enter>` and then exited the editor with `<Ctrl>X`.


## Step 5: Run the JUnit tests again

Since I already ran the two commands to compile and run the files earlier, I typed `<Ctrl>R javac <Enter>` to find the command to compile the files. Then I used `<Ctrl>R java <Space><Enter>` to find the command to run the tester file. Adding the space during the second command helps the computer differentiate between `java` and `javac`.

![Screenshot_20230226_080905](https://user-images.githubusercontent.com/122492228/221475547-a2277181-5bce-498d-938c-ea76fdf3f4dc.png)

This time, it passes both tests.

## Step 6: Commit and push changes

To commit I typed `git commit -am "edited ListExamples" <Enter>` to add the newly edited file and commit the changes with a descriptive message.

![Screenshot_20230226_081701](https://user-images.githubusercontent.com/122492228/221475637-512aa70f-6c01-4483-8f84-04d75042c1dd.png)

To then push the commit I typed `git push <Enter>`.

![Screenshot_20230226_081905](https://user-images.githubusercontent.com/122492228/221475646-33c61860-0d13-4833-aae3-b70df97f38d8.png)

