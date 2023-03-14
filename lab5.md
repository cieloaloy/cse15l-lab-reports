# Lab Report 5

This report is a retrospective on Week 6's activity about grading scripts.


## Testing Script on List Methods using implementations of ListExamples

![Screenshot 2023-03-13 211956 copy1](https://user-images.githubusercontent.com/122492228/224893917-2fec1e32-a6ea-4a63-a1b8-f1b10f2a7ebd.png)

I used nano to edit the script that my lab partner and I worked on. Our first implementation had bugs in calculating the number of tests run and passed, so I addressed those and then tested the script using three of the given implementations and our own JUnit tester. As expected, the original implementation results in two failures.

![Screenshot 2023-03-13 211956 copy2](https://user-images.githubusercontent.com/122492228/224893922-b402c41a-4916-46df-9621-899f1aa3ff63.png)

The corrected implementation results in no failures.

![Screenshot 2023-03-13 211956 copy3](https://user-images.githubusercontent.com/122492228/224893927-c6de101b-45a3-4290-9c32-c25985d7e342.png)

The compile-error implementation does not compile, and instead produces the rather harsh error message.

## Testing Script on CSE 12 PAs

I copied the grading script over to my local directory containing my CSE 12 programming assignments. I had to alter some of the paths and names used within the script so that it would look for the new correct file names. It was a bit of a struggle, as I tried using the wrong paths multiple times and it kept failing to recognize JUnit.

![Screenshot 2023-03-13 223311](https://user-images.githubusercontent.com/122492228/224905647-cc1fc669-d6e9-4c36-93d7-ac8b244c8f91.png)

Above is the altered grading script using a PA7 public tester, which passed all the tests.

![Screenshot 2023-03-13 224101](https://user-images.githubusercontent.com/122492228/224906766-2a2db962-5743-4552-b4cd-5144bcdcfa70.png)

Here is another alteration I made to run the grading script on PA6, which passed all the tests again.

![Screenshot 2023-03-13 224306](https://user-images.githubusercontent.com/122492228/224907066-45454fe1-339a-4170-92cf-5e1fad73a782.png)

I then tried my custom tester for PA6, which was very similar to using the public tester. 

Overall, using the grading script locally was pretty easy. The most difficult part was my struggle with the classpaths and using the right JUnit files in the right places.
