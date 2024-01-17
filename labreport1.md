# Lab Report 1
## CD command
1. When no argument is passed the output is:
   ![Image](http://Screenshot 2024-01-16 at 6.17.49 PM.png)
   The working directory when this command was run is /home. I got this output because the `cd` command with no arguments sets the workng directory to home which is already a given. This is not an error.
2. When an argument to a directory is passed the output is
   ![Image](Screenshot 2024-01-16 at 6.18.09 PM.png)
   The working directory when `cd lecture1` was passed is /home/lecture1. I got this output because lecture1 is inside the home             directory so when this runs we are changing from home to lecture1. This is not an error.
3. When an argument to a file is passed the output is
   ![Image](Screenshot 2024-01-16 at 6.19.51 PM.png)
   The working directory for `cd messages` is /home/lecture1/messages in this case as we are passing an argument to change the directory    to a file in lecture1 so the cd command directs to messages inside lecture1. This is not an error.
---------------------------------------
## LS command

1. When no argument is passed the output is
   ![Image](Screenshot 2024-01-16 at 6.32.17 PM.png)
   The working directory when `ls` was run is /home. I got this output because the ls command with no arguments sets the workng     directory to home which is already a given and shows the files in this working directory. This is not an error.
2. When an argument to a directory is passed the output is
   ![Image](Screenshot 2024-01-16 at 6.33.34 PM.png)
   The working directory when `ls lecture1` was passed is also /home. I got this output because the ls command does not change the           working directory, it lists what is inside the argument. This is not an error.
3. When an argument to a file is passed the output is
   ![Image](Screenshot 2024-01-16 at 6.46.35 PM.png)
   The working directory is /home/lecture1 . I got this output because the `ls Hello.java` command lists the files that are inside the      directory or file we pass as an argument. In this case we are asking it to list the file which is Hello.java, so as its output it        returns the name of the file which is a .java file. It does not list the contents. This is not an error
---------------------------------------

## CAT command
1. When no argument is passed the output is
   ![Image](Screenshot 2024-01-16 at 6.41.44 PM.png)
   The working directory when `cat` was run is /home. I got this output because the cat command with no arguments does not have      data to read from the input which is missing in this case. This is not an error.
2. When an argument to a directory is passed the output is
   ![Image](Screenshot 2024-01-16 at 6.43.52 PM.png)
   The working directory when `cat lecture1` was passed is also /home. I got this output because the cat command does not take              directories as arguments, it takes input files that it can read and output. This is not an error.
3. When an argument to a file is passed the output is
   ![Image](Screenshot 2024-01-16 at 6.44.33 PM.png)
   The working directory when `cat Hello.java` is /home/lecture1. I got this output because the cat command read the input from the         .java file we gave as an argument and was able to read and output the standard input as well as the import statements and the git        clone statement before outputting the standard input. This is not an error.


