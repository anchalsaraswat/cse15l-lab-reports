# Anchal Saraswat CSE 15L Lab Report 5

## Part 1: Student EdStem Post


**Student Post:**

List Reverse Method:

<img width="418" alt="lab5_pic1" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/a731d086-4721-4102-b32e-00525c44f4b6">

Test Output:

<img width="893" alt="lab5_pic2" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/fd20b279-3a79-4f4d-9939-53975b2a5a91">


Hi,

I'm a student taking CSE 15L this quarter and I'm running into issues when I'm trying to test my method that's supposed to reverse an array in place. When I run a Java file with JUnit, it outputs what's shown in the screenshot above. It shows that at the second index of the reversed array the expected value was 7 but the actual value was 9 which means that the method returned the wrong result. My assumption is that the input array is not being sorted properly since the last value of the original array is also the last value of the sorted array which is incorrect. I think the failure inducing input is an array of length greater than 1 and the bug is that when the method is sorting in place it's reusing values that have already been sorted at a specific index.


**TA Response:**

Hello,

My recommendation would be to run through a test of your ReverseInPlace method with an input array that has 2 or more values. This will help you understand what is going wrong since you will be running your method and keeping track of the values of the array you are reversing manually. You could also add some print statements to see which value is being swapped during each run of the loop and see if it's the correct value that should be at that index.


**Student Response:**

<img width="698" alt="lab5_pic3" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/3f746e3d-4636-44fd-be6f-cb96847e98f4">

<img width="397" alt="Screenshot 2024-03-12 at 8 07 58 PM" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/c59c2119-dc74-435b-a47f-f603c289ffea">

Thanks for the help! I decided to use print statements to see what was being replaced when the list is reversed using input {7, 8, 9}. I can see that everything is being correctly reversed except in the last run the code is swapping out 9 for 9, which is the symptom here. The list that is returned is {9, 8, 9} but it should be {9, 8, 7}. The bug here is that the array is incorrectly getting sorted because it ends up reusing indices that have already been sorted. It says "swaping 9 for 9" because when the code is at the last index it is using the first element in the sorted array which is 9. However, it’s supposed to be using the first element from the original array which is 7. 


**Information About Setup:**

File and directory structure needed:

<img width="787" alt="lab5_pic4" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/5deb82a5-e297-4474-8725-90513ed0b072">

When I list constents,  I have the test.sh file which contains the commands to run JUnit tests that would run the ArrayTests.java file, the ArrayTests.java file which contains the code to test the ReverseInPlace method, and the ReverseInPlace method which is located in ArrayExamples.java.

Content of Method File before fixing bug:

<img width="409" alt="lab5_pic5" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/95bbe0ac-b1b8-40c9-9474-32e7a74ee231">


Command I ran to trigger the bug:

`bash test.sh`

bash.sh contains: 

<img width="816" alt="lab5_pic6" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/f35f9ca2-b072-4d7f-96ff-c98b45c96692">


How to fix bug:


To debug I used two pointers as indices of the array. Of these two, one starts at the 0th index and the second starts at the last index, then I swap these two values by saving the value of the left pointer in a variable and setting the value of left pointer to the right one. I then update the right pointer with the saved left value and increase left pointer by 1 and decrease right pointer by 1 which moves them closer to the center of the array. The loop then continues until both pointers reach the middle which means the array has been reversed.
```
static void reverseInPlace(int[] arr) {
    int left = 0;
    int right = arr.length - 1;
    while (left < right) {
        int val = arr[left];
        arr[left] = arr[right];
        arr[right] = val;
        left++;
        right--;
    }
}
```

## Part 2: Reflection:

Something I learned from my lab experience in the second half of this quarter is how to use vim. Vim is very useful in debugging and it while it was tedious to learn commands and get used to making these commands second nature, they helped a lot when I wanted to open files on my computer and I didn't have VSCode or other platforms to use. Debugging is also a skill that is always needed in future classes and in the workplace so being able to step through a program and debug is something I found pretty cool and am glad I was able to learn.


