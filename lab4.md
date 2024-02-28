# Anchal Saraswat CSE 15L Lab Report 4

## Step 1: Connect to ieng6

Command: `ssh asaraswat@ieng6.ucsd.edu`

**Keys Pressed:** *`<up> <up> <up> <up> <up> <up> <up> <up> <Enter>` 
The `ssh asaraswat@ieng6.ucsd.edu` command was used 8 commands ago, I pressed the up arrow 8 times to get to that command and then ran to connect to ieng6


<img width="780" alt="lab4pic1" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/c4d0a059-b109-42be-9554-67c5f95613d4">


## Step 2: Clone repository with SSH url

Command: `git clone git@github.com:anchalsaraswat/lab7.git` `cd lab7`


**Keys Pressed:** *`Ctrl-C: git clone git@github.com:anchalsaraswat/lab7.git` `Typed on command line: git clone` `Ctrl-V` `<Enter>`*
I used `Ctrl-C` to copy the ssh clone URL from my forked lab7 Github repository and then pasted with `Ctrl-V` after the `git clone`. Then I pressed enter to run the completed command to clone the forked repository and then `cd lab7` to change the directory to the lab7 repo


<img width="549" alt="lab4pic2" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/2692d018-6e84-4187-af56-91444c9bd194">


## Step 3: Running JUnit Tests with ListExampleTests

Commands:
1. `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar`

**Keys Pressed:** *`<up> <up> <up> <up> <up> <Enter>`* The `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command was used 5 commands ago so I pressed the up arrow 5 times to get to that command and then ran 

2. `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`
   
**Keys Pressed:** *`<up> <up> <up> <up> <up> <Enter>`* After running previous command to compile JUnit Test, the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` was used 5 commands ago, so I pressed the up arrow 5 times to get to that command and then ran it to run ListExamplesTests
   
<img width="774" alt="lab4pic3" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/d0fb3cc4-d5d4-43e3-a9fb-2ca5d9d0190c">

## Step 4: Edit the code to fix the failing test

**Open File in vim before editing:** 

**Keys Pressed:** `vim ListExamples.java` `<Enter>`

**Edit ListExamples.java File in vim:**

**Keys Pressed:** from cursor at top, left of the file: `329w`, `e`, `x`, `i`, `"2"`, `<esc>` `:wq`
After opening ListExamples.java file in vim my cursor was at the top left of the file and I wanted to move the cursor to the line with the bug so I moved the cursor forward 329 words with `329w`, moved to the end of the current word "index" with `e` to land on "1" of `index1`. Then I pressed `x` to delete the "1", pressed `i` to enter insert mode, entered "2" to change the variable to `index2`.Then I pressed `<esc>` to go back to normal mode and then used `:wq` to save and exit the file.

<img width="616" alt="lab4pic4" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/069ddadd-54e1-49c3-ada5-6b23ed561a7e">


## Step 5: Run the tests to show that they now succeed

Commands: 
1. `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`

**Keys Pressed:** `<up> <up> <up>` `<Enter>`
The `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command was used 3 commands ago so I pressed the up arrow 3 times to get to that command and then ran 


2. `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` 

**Keys Pressed:** `<up> <up> <up>` `<Enter>`
After running the previous command to compile JUnit Test, the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` was used 5 commands ago so I pressed the up arrow 5 times to get to that command and then ran it to run ListExamplesTests

<img width="780" alt="lab4pic5" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/c217f142-6c34-4c36-9320-bfc36e77c5c2">


## Step 6: Commit and push changes to Github

**Keys Pressed:** `git add ListExamples.java` `<Enter>` `git commit -m"changed var"` `<Enter>` `git push` `<Enter>`
After debugging and making edits to ListExamples.java I need these changes to show on the remote repository on Github so I do `git add` from the command line to add `ListExamples.java` as a file to be included for the commit message and then I can create the commit with a message "changed var" through `git commit -m"changed var"`. Then I push the changes to my Github repository with `git push` and the edits I commited will show up on GitHub

<img width="722" alt="lab4pic6" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/83496f79-b490-4d69-857b-8c8dc0c71369">
